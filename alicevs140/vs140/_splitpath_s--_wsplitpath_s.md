---
title: "_splitpath_s, _wsplitpath_s"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
  - C
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
apiname: 
  - _wsplitpath_s
  - _splitpath_s
apilocation: 
  - msvcr90.dll
  - msvcr110_clr0400.dll
  - msvcrt.dll
  - msvcr100.dll
  - msvcr120.dll
  - msvcr110.dll
  - msvcr80.dll
  - msvcr120_clr0400.dll
apitype: DLLExport
ms.assetid: 30fff3e2-cd00-4eb6-b5a2-65db79cb688b
caps.latest.revision: 31
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _splitpath_s, _wsplitpath_s
Breaks a path name into components. These are versions of [_splitpath, _wsplitpath](../vs140/_splitpath--_wsplitpath.md) with security enhancements as described in [Security Enhancements in the CRT](../vs140/Security-Features-in-the-CRT.md).  
  
## Syntax  
  
```  
errno_t _splitpath_s(  
   const char * path,  
   char * drive,  
   size_t driveNumberOfElements,  
   char * dir,  
   size_t dirNumberOfElements,  
   char * fname,  
   size_t nameNumberOfElements,  
   char * ext,   
   size_t extNumberOfElements  
);  
errno_t _wsplitpath_s(  
   const wchar_t * path,  
   wchar_t * drive,  
   size_t driveNumberOfElements,  
   wchar_t *dir,  
   size_t dirNumberOfElements,  
   wchar_t * fname,  
   size_t nameNumberOfElements,  
   wchar_t * ext,  
   size_t extNumberOfElements  
);  
template <size_t drivesize, size_t dirsize, size_t fnamesize, size_t extsize>  
errno_t _splitpath_s(  
   const char *path,  
   char (&drive)[drivesize],  
   char (&dir)[dirsize],  
   char (&fname)[fnamesize],  
   char (&ext)[extsize]  
); // C++ only  
template <size_t drivesize, size_t dirsize, size_t fnamesize, size_t extsize>  
errno_t _wsplitpath_s(  
   const wchar_t *path,  
   wchar_t (&drive)[drivesize],  
   wchar_t (&dir)[dirsize],  
   wchar_t (&fname)[fnamesize],  
   wchar_t (&ext)[extsize]  
); // C++ only  
```  
  
#### Parameters  
 [in] `path`  
 Full path.  
  
 [out] `drive`  
 Drive letter, followed by a colon (`:`). You can pass `NULL` for this parameter if you do not need the drive letter.  
  
 [in] `driveNumberOfElements`  
 The size of the `drive` buffer in single-byte or wide characters. If `drive` is `NULL`, this value must be 0.  
  
 [out] `dir`  
 Directory path, including trailing slash. Forward slashes ( `/` ), backslashes ( `\` ), or both may be used. You can pass `NULL` for this parameter if you do not need the directory path.  
  
 [in] `dirNumberOfElements`  
 The size of the `dir` buffer in single-byte or wide characters. If `dir` is `NULL`, this value must be 0.  
  
 [out] `fname`  
 Base filename (without extension). You can pass `NULL` for this parameter if you do not need the filename.  
  
 [in] `nameNumberOfElements`  
 The size of the `fname` buffer in single-byte or wide characters. If `fname` is `NULL`, this value must be 0.  
  
 [out] `ext`  
 Filename extension, including leading period (**.**).You can pass `NULL` for this parameter if you do not need the filename extension.  
  
 [in] `extNumberOfElements`  
 The size of `ext` buffer in single-byte or wide characters. If `ext` is `NULL`, this value must be 0.  
  
## Return Value  
 Zero if successful; an error code on failure.  
  
### Error Conditions  
  
|Condition|Return Value|  
|---------------|------------------|  
|`path` is `NULL`|`EINVAL`|  
|`drive` is `NULL`, `driveNumberOfElements` is non-zero|`EINVAL`|  
|`drive` is non-`NULL`, `driveNumberOfElements` is zero|`EINVAL`|  
|`dir` is `NULL`, `dirNumberOfElements` is non-zero|`EINVAL`|  
|`dir` is non-`NULL`, `dirNumberOfElements` is zero|`EINVAL`|  
|`fname` is `NULL`, `nameNumberOfElements` is non-zero|`EINVAL`|  
|`fname` is non-`NULL`, `nameNumberOfElements` is zero|`EINVAL`|  
|`ext` is `NULL`, `extNumberOfElements` is non-zero|`EINVAL`|  
|`ext` is non-`NULL`, `extNumberOfElements` is zero|`EINVAL`|  
  
 If any of the above conditions occurs, the invalid parameter handler is invoked, as described in [Parameter Validation](../vs140/Parameter-Validation.md) . If execution is allowed to continue, these functions set `errno` to `EINVAL` and return `EINVAL`.  
  
 If any of the buffers is too short to hold the result, these functions clear all the buffers to empty strings, set `errno` to `ERANGE`, and return `ERANGE`.  
  
## Remarks  
 The `_splitpath_s` function breaks a path into its four components. `_splitpath_s` automatically handles multibyte-character string arguments as appropriate, recognizing multibyte-character sequences according to the multibyte code page currently in use. `_wsplitpath_s` is a wide-character version of `_splitpath_s`; the arguments to `_``wsplitpath_s`are wide-character strings. These functions behave identically otherwise  
  
### Generic-Text Routine Mappings  
  
|TCHAR.H routine|_UNICODE & _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|------------------------------------|--------------------|-----------------------|  
|`_tsplitpath_s`|`_splitpath_s`|`_splitpath_s`|`_wsplitpath_s`|  
  
 Each component of the full path is stored in a separate buffer; the manifest constants `_MAX_DRIVE`, `_MAX_DIR`, `_MAX_FNAME`, and `_MAX_EXT` (defined in STDLIB.H) specify the maximum allowable size for each file component. File components larger than the corresponding manifest constants cause heap corruption.  
  
 The following table lists the values of the manifest constants.  
  
|Name|Value|  
|----------|-----------|  
|_MAX_DRIVE|3|  
|_MAX_DIR|256|  
|_MAX_FNAME|256|  
|_MAX_EXT|256|  
  
 If the full path does not contain a component (for example, a filename), `_splitpath_s` assigns an empty string to the corresponding buffer.  
  
 In C++, using these functions is simplified by template overloads; the overloads can infer buffer length automatically, eliminating the need to specify a size argument. For more information, see [Secure Template Overloads](../vs140/Secure-Template-Overloads.md).  
  
 The debug versions of these functions first fill the buffer with 0xFD. To disable this behavior, use [_CrtSetDebugFillThreshold](../vs140/_CrtSetDebugFillThreshold.md).  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_splitpath_s`|<stdlib.h>|  
|`_wsplitpath_s`|<stdlib.h> or <wchar.h>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Example  
 See the example for [_makepath_s](../vs140/_makepath_s--_wmakepath_s.md).  
  
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [File Handling](../Topic/File%20Handling.md)   
 [_splitpath, _wsplitpath](../vs140/_splitpath--_wsplitpath.md)   
 [_fullpath, _wfullpath](../vs140/_fullpath--_wfullpath.md)   
 [_getmbcp](../vs140/_getmbcp.md)   
 [_makepath, _wmakepath](../vs140/_makepath--_wmakepath.md)   
 [_setmbcp](../vs140/_setmbcp.md)