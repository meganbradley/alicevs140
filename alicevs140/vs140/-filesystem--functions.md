---
title: "&lt;filesystem&gt; functions"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: be3cb821-4728-4d47-ab78-858fa8aa5045
caps.latest.revision: 14
translation.priority.mt: 
  - de-de
  - ja-jp
---
# &lt;filesystem&gt; functions
These free functions in the [<filesystem\> (v3)](../vs140/-filesystem-.md) header perform modifying and query operations on paths, files, symlinks, directories and volumes. For more information and code examples, see [File System Navigation](../vs140/File-System-Navigation.md).  
  
## absolute  
  
```  
path absolute(const path& pval, const path& base = current_path());  
  
```  
  
 The function returns the absolute pathname corresponding to `pval` relative to the pathname `base`:  
  
1.  If pval.has_root_name() && pval.has_root_directory() the function returns pval.  
  
2.  If pval.has_root_name() && !pval.has_root_directory() the function returns pval.root_name() / absolute(base).root_directory() / absolute(base).relative_path() / pval.relative_path().  
  
3.  If !pval.has_root_name() && pval.has_root_directory() the function returns absolute(base).root_name() / pval.  
  
4.  If !pval.has_root_name() && !pval.has_root_directory() the function returns absolute(base) / pval.  
  
## begin  
  
```  
const directory_iterator& begin(const directory_iterator& iter) noexcept;  
const recursive_directory_iterator&  
    begin(const recursive_directory_iterator& iter) noexcept;  
  
```  
  
 Both functions return `iter`.  
  
## canonical  
  
```  
path canonical(const path& pval, const path& base = current_path());  
path canonical(const path& pval,  
    error_code& ec);  
path canonical(const path& pval, const path& base,  
    error_code& ec);  
```  
  
 The functions all form an absolute pathname pabs = absolute(pval, base) (or pabs = absolute(pval) for the overload with no base parameter), then reduce it to a canonical form in the following sequence of steps:  
  
1.  Every path component X for which is_symlink(X) is true is replaced by read_symlink(X).  
  
2.  Every path component . (dot is the current directory established by previous path components) is removed.  
  
3.  Every pair of path components X/.. (dot-dot is the parent directory established by previous path components) is removed.  
  
 The function then returns pabs.  
  
## copy  
  
```  
void copy(const path& from, const path& to);  
void copy(const path& from, const path& to,  
    error_code& ec) noexcept;  
void copy(const path& from, const path& to, copy_options opts);  
void copy(const path& from, const path& to, copy_options opts,  
    error_code& ec) noexcept;  
```  
  
 The functions all possibly copy or link one or more files at `from` to `to` under control of `opts`, which is taken as copy_options::none for the overloads with no `opts` parameter. `opts` shall contain at most one of:  
  
-   skip_existing, overwrite_existing, or update_existing  
  
-   copy_symlinks or skip_symlinks  
  
-   directories_only, create_symlinks, or create_hard_links  
  
 The functions first determine the file_status values f for `from` and t for `to`:  
  
-   if opts & (copy_options::create_symlinks &#124; copy_options::skip_symlinks), by calling symlink_status  
  
-   otherwise, by calling status  
  
-   Otherwise report an error.  
  
 If !exists(f) &#124;&#124; equivalent(f, t) &#124;&#124; is_other(f) &#124;&#124; is_other(t) &#124;&#124; is_directory(f)&& is_regular_file(t), they then report an error (and do nothing else).  
  
 Otherwise, if is_symlink(f) then:  
  
-   If options & copy_options::skip_symlinks then do nothing.  
  
-   Otherwise, if !exists(t)&& options & copy_options::copy_symlinks then copy_symlink(from, to, opts).  
  
-   Otherwise report an error.  
  
 Otherwise, if is_regular_file(f) then:  
  
-   If opts & copy_options::directories_only then do nothing.  
  
-   Otherwise, if opts & copy_options::create_symlinks then create_symlink(to, from).  
  
-   Otherwise, if opts & copy_options::create_hard_links then create_hard_link(to, from).  
  
-   Otherwise, if is_directory(f) then copy_file(from, to / from.filename(), opts).  
  
-   Otherwise, copy_file(from, to, opts).  
  
 Otherwise, if is_directory(f) && (opts & copy_options::recursive &#124;&#124; !opts) then:  
  
-   ```  
    if (!exists(t))  
        {  // copy directory contents recursively  
        create_directory(to, from, ec);  
        for (directory_iterator next(from), end;  
            ec == error_code() && next != end; ++next)  
            copy(next->path(),  
                to / next->path().filename(), opts, ec);  
        }  
    ```  
  
 Otherwise, do nothing.  
  
## copy\_file  
  
```  
bool copy_file(const path& from, const path& to);  
bool copy_file(const path& from, const path& to,  
    error_code& ec) noexcept;  
bool copy_file(const path& from, const path& to, copy_options opts);  
bool copy_file(const path& from, const path& to, copy_options opts,  
    error_code& ec) noexcept;  
```  
  
 The functions all possibly copy the file at `from` to `to` under control of `opts`, which is taken as copy\_options::none for the overloads with no `opts` parameter. `opts` shall contain at most one of skip\_existing, overwrite\_existing, or update\_existing.  
  
 If exists\(to\) && \!\(opts & \(copy\_options::skip\_existing &#124; copy\_options::overwrite\_existing &#124; copy\_options::update\_existing\)\) then report as an error that the file already exists.  
  
 Otherwise, if \!exists\(to\) &#124;&#124; opts & copy\_options::overwrite\_existing &#124;&#124; opts & copy\_options::update\_existing&& last\_write\_time\(to\) \< last\_write\_time\(from\) &#124;&#124; \!\(opts & \(copy\_options::skip\_existing &#124; copy\_options::overwrite\_existing &#124; copy\_options:update\_existing\)\) then attempt to copy the contents and attributes of the file from to the file to. Report as an error if the copy attempt fails.  
  
 The functions return true if the copy is attempted and succeeds, otherwise false.  
  
## copy\_symlink  
  
```  
void copy_symlink(const path& from, const path& to);  
void copy_symlink(const path& from, const path& to,  
    error_code& ec) noexcept;  
```  
  
 If is\_directory\(from\) the function calls create\_directory\_symlink\(from, to\). Otherwise, it calls create\_symlink\(from, to\).  
  
## create\_directories  
  
```  
bool create_directories(const path& pval);  
bool create_directories(const path& pval,  
    error_code& ec) noexcept;  
```  
  
 For a pathname such as a\/b\/c the function creates directories a and a\/b as needed so that it can create the directory a\/b\/c as needed. It returns true only if it actually creates the directory `pval`.  
  
## create\_directory  
  
```  
bool create_directory(const path& pval);  
bool create_directory(const path& pval,  
    error_code& ec) noexcept;  
bool create_directory(const path& pval, const path& attr);  
bool create_directory(const path& pval, const path& attr,  
    error_code& ec) noexcept;  
```  
  
 The function creates the directory `pval` as needed. It returns true only if it actually creates the directory `pval`, in which case it copies permissions from the existing file `attr`, or uses perms::all for the overloads with no `attr` parameter.  
  
## create\_directory\_symlink  
  
```  
void create_directory_symlink(const path& to, const path& link);  
void create_directory_symlink(const path& to, const path& link),  
    error_code& ec) noexcept;  
```  
  
 The function creates link as a symlink to the directory `to`.  
  
## create\_hard\_link  
  
```  
void create_hard_link(const path& to, const path& link);  
void create_hard_link(const path& to, const path& link),  
    error_code& ec) noexcept;  
```  
  
 The function creates link as a hard link to the directory or file `to`.  
  
## create\_symlink  
  
```  
void create_symlink(const path& to, const path& link);  
void create_symlink(const path& to, const path& link),  
    error_code& ec) noexcept;  
```  
  
 The function creates `link` as a symlink to the file `to`.  
  
## current\_path  
  
```  
path current_path();  
path current_path(  
    error_code& ec);  
void current_path(const path& pval);  
void current_path(const path& pval,  
    error_code& ec) noexcept;  
```  
  
 The functions with no parameter `pval` return the pathname for the current directory. The remaining functions set the current directory to `pval`.  
  
## end  
  
```  
directory_iterator& end(const directory_iterator& iter) noexcept;  
recursive_directory_iterator&  
    end(const recursive_directory_iterator& iter) noexcept;  
```  
  
 The first function returns directory\_iterator\(\) and the second function returns recursive\_directory\_iterator\(\)  
  
## equivalent  
  
```  
bool equivalent(const path& left, const path& right);  
bool equivalent(const path& left, const path& right,  
    error_code& ec) noexcept;  
```  
  
 The functions return true only if `left` and `right` designate the same filesystem entity.  
  
## exists  
  
```  
bool exists(file_status stat) noexcept;  
bool exists(const path& pval);  
bool exists(const path& pval,  
    error_code& ec) noexcept;  
```  
  
 The first function returns status\_known && stat.type\(\) \!\= file\_not\_found. The second and third functions return exists\(status\(pval\)\).  
  
## file\_size  
  
```  
uintmax_t file_size(const path& pval);  
uintmax_t file_size(const path& pval,  
    error_code& ec) noexcept;  
```  
  
 The functions return the size in bytes of the file designated by `pval`, if exists\(pval\) && is\_regular\_file\(pval\) and the file size can be determined. Otherwise they report an error and return uintmax\_t\(\-1\).  
  
## hard\_link\_count  
  
```  
uintmax_t hard_link_count(const path& pval);  
uintmax_t hard_link_count(const path& pval,  
    error_code& ec) noexcept;  
```  
  
 The function returns the number of hard links for `pval`, or \-1 if an error occurs.  
  
## hash\_value  
  
```  
size_t hash_value(const path& pval) noexcept;  
```  
  
 The function returns a hash value for pval.native\(\).  
  
## is\_block\_file  
  
```  
bool is_block_file(file_status stat) noexcept;  
bool is_block_file(const path& pval);  
bool is_block_file(const path& pval,  
    error_code& ec) noexcept;  
  
```  
  
 The first function returns stat.type\(\) \=\= file\_type::block. The remaining functions return is\_block\_file\(status\(pval\)\).  
  
## is\_character\_file  
  
```  
  
bool is_character_file(file_status stat) noexcept;  
bool is_character_file(const path& pval);  
bool is_character_file(const path& pval,  
    error_code& ec) noexcept;  
  
```  
  
 The first function returns stat.type\(\) \=\= file\_type::character. The remaining functions return is\_character\_file\(status\(pval\)\).  
  
## is\_directory  
  
```  
  
bool is_directory(file_status stat) noexcept;  
bool is_directory(const path& pval);  
bool is_directory(const path& pval,  
    error_code& ec) noexcept;  
  
```  
  
 The first function returns stat.type\(\) \=\= file\_type::directory. The remaining functions return is\_directory\_file\(status\(pval\)\).  
  
## is\_empty  
  
```  
  
bool is_empty(file_status stat) noexcept;  
bool is_empty(const path& pval);  
bool is_empty(const path& pval,  
    error_code& ec) noexcept;  
  
```  
  
 If is\_directory\(pval\) then the function returns directory\_iterator\(pval\) \=\= directory\_iterator\(\); otherwise it returns file\_size\(pval\) \=\= 0.  
  
## is\_fifo  
  
```  
bool is_fifo(file_status stat) noexcept;  
bool is_fifo(const path& pval);  
bool is_fifo(const path& pval,  
    error_code& ec) noexcept;  
  
```  
  
 The first function returns stat.type\(\) \=\= file\_type::fifo. The remaining functions return is\_fifo\(status\(pval\)\).  
  
## is\_other  
  
```  
bool is_other(file_status stat) noexcept;  
bool is_other(const path& pval);  
bool is_other(const path& pval,  
    error_code& ec) noexcept;  
  
```  
  
 The first function returns stat.type\(\) \=\= file\_type::other. The remaining functions return is\_other\(status\(pval\)\).  
  
## is\_regular\_file  
  
```  
  
bool is_regular_file(file_status stat) noexcept;  
bool is_regular_file(const path& pval);  
bool is_regular_file(const path& pval,  
    error_code& ec) noexcept;  
  
```  
  
 The first function returns stat.type\(\) \=\= file\_type::regular. The remaining functions return is\_regular\_file\(status\(pval\)\).  
  
## is\_socket  
  
```  
  
bool is_socket(file_status stat) noexcept;  
bool is_socket(const path& pval);  
bool is_socket(const path& pval,  
    error_code& ec) noexcept;  
  
```  
  
 The first function returns stat.type\(\) \=\= file\_type::socket. The remaining functions return is\_socket\(status\(pval\)\).  
  
## is\_symlink  
  
```  
  
bool is_symlink(file_status stat) noexcept;  
bool is_symlink(const path& pval);  
bool is_symlink(const path& pval,  
    error_code& ec) noexcept;  
  
```  
  
 The first function returns stat.type\(\) \=\= file\_type::symlink. The remaining functions return is\_symlink\(status\(pval\)\).  
  
## last\_write\_time  
  
```  
  
file_time_type last_write_time(const path& pval);  
file_time_type last_write_time(const path& pval,  
    error_code& ec) noexcept;  
void last_write_time(const path& pval, file_time_type new_time);  
void last_write_time(const path& pval, file_time_type new_time,  
    error_code& ec) noexcept;  
  
```  
  
 The first two functions return the time of last data modification for `pval`, or file\_time\_type\(\-1\) if an error occurs. The last two functions set the time of last data modification for `pval` to new\_time.  
  
## permissions  
  
```  
void permissions(const path& pval, perms mask);  
void permissions(const path& pval, perms mask,  
    error_code& ec) noexcept;  
  
```  
  
 The functions set the permissions for the pathname designated by `pval` to mask & perms::mask under control of perms & \(perms::add\_perms &#124; perms::remove\_perms\). mask shall contain at most one of perms::add\_perms and perms::remove\_perms.  
  
 If mask & perms::add\_perms the functions set the permissions to status\(pval\).permissions\(\) &#124; mask & perms::mask. Otherwise, if mask & perms::remove\_perms the functions set the permissions to status\(pval\).permissions\(\) & ~\(mask & perms::mask\). Otherwise, the functions set the permissions to mask & perms::mask.  
  
## read\_symlink  
  
```  
path read_symlink(const path& pval);  
path read_symlink(const path& pval.  
    error_code& ec);  
```  
  
 The functions report an error and return path\(\) if \!is\_symlink\(pval\). Otherwise, the functions return an object of type `path` containing the symbolic link.  
  
## remove  
  
```  
bool remove(const path& pval);  
bool remove(const path& pval,  
    error_code& ec) noexcept;  
```  
  
 The functions return true only if exists\(symlink\_status\(pval\)\) and the file is successfully removed. A symlink is itself removed, not the file it designates.  
  
## remove\_all  
  
```  
uintmax_t remove_all(const path& pval);  
uintmax_t remove_all(const path& pval,  
    error_code& ec) noexcept;  
  
```  
  
 If `pval` is a directory, the functions recursively remove all directory entries, then the entry itself. Otherwise, the functions call remove. They return a count of all elements successfully removed.  
  
## rename  
  
```  
void rename(const path& from, const path& to);  
void rename(const path& from, const path& to,  
    error_code& ec) noexcept;  
```  
  
 The functions rename `from` to `to`. A symlink is itself renamed, not the file it designates.  
  
## resize\_file  
  
```  
void resize(const path& pval, uintmax_t size);  
void resize(const path& pval, uintmax_t size,  
    error_code& ec) noexcept;  
```  
  
 The functions alter the size of a file such that file\_size\(pval\) \=\= size  
  
## space  
  
```  
space_info space(const path& pval);  
space_info space(const path& pval,  
    error_code& ec) noexcept;  
```  
  
 The function returns information about the volume designated by `pval`, in a structure of type `space_info`. The structure contains uintmax\_t\(\-1\) for any value that cannot be determined.  
  
## status  
  
```  
file_status status(const path& pval);  
file_status status(const path& pval,  
    error_code& ec) noexcept;  
  
```  
  
 The functions return the pathname status, the file type and permissions, associated with `pval`. A symlink is itself not tested, but the file it designates.  
  
## status\_known  
  
```  
bool status_known(file_status stat) noexcept;  
```  
  
 The function returns stat.type\(\) \!\= file\_type::none  
  
## swap  
  
```  
void swap(path& left, path& right) noexcept;  
  
```  
  
 The function exchanges the contents of `left` and `right`.  
  
## symlink\_status  
  
```  
file_status symlink_status(const path& pval);  
file_status symlink_status(const path& pval,  
    erroxr_code& ec) noexcept;  
  
```  
  
 The functions return the pathname symlink status, the file type and permissions, associated with `pval`. The functions behave the same as status\(pval\) except that a symlink is itself tested, not the file it designates.  
  
## system\_complete  
  
```  
path system_complete(const path& pval);  
path system_complete(const path& pval,  
    error_code& ec);  
  
```  
  
 The functions return an absolute pathname that takes into account, as necessary, the current directory associated with its root name. \(For Posix, the functions return absolute\(pval\).\)  
  
## temp\_directory\_path  
  
```  
path temp_directory_path();  
path temp_directory_path(  
    error_code& ec);  
  
```  
  
 The functions return a pathname for a directory suitable for containing temporary files.  
  
## u8path  
  
```  
template<class Source>  
    path u8path(const Source& source);  
template<class InIt>  
    path u8path(InIt first, InIt last);  
  
```  
  
 The first function behaves the same as path(source) and the second function behaves the same as path(first, last) except that the designated source in each case is taken as a sequence of char elements encoded as UTF-8, regardless of the filesystem.