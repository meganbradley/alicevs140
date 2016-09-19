---
title: "File System Navigation"
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
ms.assetid: f7cc5f5e-a541-4e00-87c7-a3769ef6096d
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# File System Navigation
The <filesystem\> header implements the C++ File System Technical Specification ISO/IEC TS 18822:2015 (Final draft: [ISO/IEC JTC 1/SC 22/WG 21 N4100](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2014/n4100.pdf)) and has types and functions that enable you to write platform-independent code for navigating the file system. Because it is cross-platform, it contains APIs that are not relevant for Windows systems. For example, this means that `is_fifo(const path&)` always returns `false` on Windows. The header is based on a draft Technical Specification that was not voted into the C++17 standard as of Visual Studio 2015 RTM. Its members are found in the  `std::experimental::filesystem::v1` namespace.  
  
## Overview  
 Use the <filesystem\> APIs for the following tasks:  
  
-   iterate over files and directories under a specified path  
  
-   get information about files including the time created, size, extension, and root directory  
  
-   compose, decompose, and compare paths  
  
-   create, copy and delete directories  
  
-   copy and delete files  
  
 For more information about File IO using the Standard Library, see [iostream Programming](../vs140/iostream-Programming.md).  
  
## Paths  
  
### Constructing and composing paths  
 Paths in Windows (since XP) are stored natively in Unicode. The [path](../vs140/path-Class--C---Standard-Template-Library-.md) class automatically performs all necessary string conversions. It accepts arguments of both wide and narrow character arrays, as well as `std::string` and `std::wstring` types formatted as UTF8 or UTF16. The `path` class also automatically normalizes path separators. You can use a single forward slash as a directory separator in constructor arguments. This enables you to use the same strings to store paths in both Windows and UNIX environments:  
  
```cpp  
path pathToDisplay(L"/FileSystemTest/SubDir3"); // OK!  
path pathToDisplay2(L"\\FileSystemTest\\SubDir3"); // Still OK as always  
path pathToDisplay3(LR"(\FileSystemTest\SubDir3)"); // Raw string literals are OK, too.  
```  
  
 To concatenate two paths, you can use the overloaded `/` and `/=` operators, which are analogous to the `+` and `+=` operators on `std::string` and `std::wstring`. The `path` object will conveniently supply the separators if you don’t.  
  
```cpp  
path myRoot("C:/FileSystemTest"); // no trailing separator, no problem!  
myRoot /= path("SubDirRoot"); // C:/FileSystemTest/SubDirRoot  
```  
  
### Examining paths  
 The path class has several methods that return information about various parts of the path itself, as distinct from the file system entity it might refer to. You can get the root, the relative path, the file name, the file extension, and more. You can iterate over a path object to examine all the folders in the hierarchy. The following example shows how to iterate over a path (not the directory it refers to), and to retrieve information about its parts.  
  
```cpp  
  
#include <string>  
#include <iostream>  
#include <sstream>  
#include <filesystem>  
  
using namespace std;  
using namespace std::experimental::filesystem::v1;  
  
wstring  DisplayPathInfo()  
{  
    // This path may or may not refer to an existing file. We are   
    // examining this path string, not file system objects.  
    path pathToDisplay(L"C:/FileSystemTest/SubDir3/SubDirLevel2/File2.txt ");  
  
    wostringstream wos;  
    int i = 0;  
    wos << L"Displaying path info for: " << pathToDisplay << endl;  
    for (path::iterator itr = pathToDisplay.begin(); itr != pathToDisplay.end(); ++itr)  
    {  
        wos << L"path part: " << i++ << L" = " << *itr << endl;  
    }  
  
    wos << L"root_name() = " << pathToDisplay.root_name() << endl  
        << L"root_path() = " << pathToDisplay.root_path() << endl  
        << L"relative_path() = " << pathToDisplay.relative_path() << endl  
        << L"parent_path() = " << pathToDisplay.parent_path() << endl  
        << L"filename() = " << pathToDisplay.filename() << endl  
        << L"stem() = " << pathToDisplay.stem() << endl  
        << L"extension() = " << pathToDisplay.extension() << endl;  
  
    return wos.str();  
}  
  
void main(int argc, char* argv[])  
{  
    wcout << DisplayPathInfo() << endl;  
    // wcout << ComparePaths() << endl; // see following example  
    wcout << endl << L"Press Enter to exit" << endl;  
    wstring input;  
    getline(wcin, input);  
}  
```  
  
 The code produces this output:  
  
```cpp  
Displaying path info for: C:\FileSystemTest\SubDir3\SubDirLevel2\File2.txt  
path part: 0 = C:  
path part: 1 = \  
path part: 2 = FileSystemTest  
path part: 3 = SubDir3  
path part: 4 = SubDirLevel2  
path part: 5 = File2.txt  
root_name() = C:  
root_path() = C:\  
relative_path() = FileSystemTest\SubDir3\SubDirLevel2\File2.txt  
parent_path() = C:\FileSystemTest\SubDir3\SubDirLevel2  
filename() = File2.txt  
stem() = File2  
extension() = .txt  
```  
  
### Comparing paths  
 The `path` class overloads the same comparison operators as `std::string` and `std::wstring`. When you compare two paths, you are performing a string comparison after the separators have been normalized. If a trailing slash (or backslash) is missing it is not added and affects the comparison. The following example demonstrates how path values compare:  
  
```cpp  
  
wstring ComparePaths()  
{  
    path p0(L"C:/Documents"); // no trailing separator  
    path p1(L"C:/Documents/"); //p0 < p1  
    path p2(L"C:/Documents/2013/"); // p1 < p2      
    path p3(L"C:/Documents/2013/Reports/"); // p2 < p3  
    path p4(L"C:/Documents/2014/");  // p3 < p4   
    path p5(L"D:/Documents/2013/Reports/"); // p4 < p5  
  
    wostringstream wos;  
    wos << boolalpha <<  
        p0.wstring() << L" < " << p1.wstring() << L": " << (p0 < p1) << endl <<  
        p1.wstring() << L" < " << p2.wstring() << L": " << (p1 < p2) << endl <<  
        p2.wstring() << L" < " << p3.wstring() << L": " << (p2 < p3) << endl <<  
        p3.wstring() << L" < " << p4.wstring() << L": " << (p3 < p4) << endl <<  
        p4.wstring() << L" < " << p5.wstring() << L": " << (p4 < p5) << endl;  
    return wos.str();  
}  
/* Output:  
C:\Documents < C:\Documents\: true  
C:\Documents\ < C:\Documents\2013\: true  
C:\Documents\2013\ < C:\Documents\2013\Reports\: true  
C:\Documents\2013\Reports\ < C:\Documents\2014\: true  
C:\Documents\2014\ < D:\Documents\2013\Reports\: true  
*/  
```  
  
 To run this code, paste it into the full example above and uncomment the line that calls it in main.  
  
### Converting between path and string types  
 A `path` object is implicitly convertible to `std::wstring` or `std::string`. This means you can pass a path to functions such as [wofstream::open](../vs140/basic_ofstream--open.md), as shown in this example:  
  
```cpp  
wchar_t* p = L"C:/test";  
    path filePath(p);  
    filePath /= L"NewFile.txt";  
  
    // Open, write to, and close the file.  
    wofstream myFile;  
    myFile.open(filePath);  
    myFile << L"Lorem ipsum...";  
    myFile.close  
  
```  
  
## Iterating directories and files  
 The <filesystem\> header provides the [directory_iterator](../vs140/directory_iterator-Class.md) type to iterate over single directories, and the [recursive_directory_iterator](../vs140/recursive_directory_iterator-Class.md) class to iterate recursively over a directory and its subdirectories. After you construct an iterator by passing it a `path` object, the iterator points to the first directory_entry in the path. Create the end iterator by calling the default constructor.  
  
 When iterating through a directory, there are several kinds of items you might encounter, including but not limited to directories, files, symbolic links, and socket files. The `directory_iterator` returns its items as [directory_entry](../vs140/directory_entry-Class.md) objects, and each object has a [status()](assetId:///a70a3c55-3a76-417f-abaf-862ff94b2056) member that tells what kind of entry you are looking at. By examining this value, you can make decisions about what to do for any particular entry. The following example iterates over a single directory, and if the directory entry is a regular file, the code prints out some information about that file. If the entry is a directory, only the name is displayed.  
  
```cpp  
#include <string>  
#include <iostream>  
#include <iomanip>  
#include <filesystem>  
#include <chrono>  
#include <time.h>  
  
using namespace std;  
using namespace std::experimental::filesystem::v1;  
  
// Display the last write time for the file  
wstring LastWriteTimeToLocalTime(const path& file_path)  
{  
    const auto last = chrono::system_clock::to_time_t(last_write_time(file_path));  
    tm timeinfo;  
    localtime_s(&timeinfo, &last);  
    wchar_t buf[56];  
    _wasctime_s(buf, 56, &timeinfo); // appends '\n'  
    return wstring{ buf };  
}  
  
// List files and directories in the specified path  
void DisplayFolderContents(const path& p)  
{  
    wcout << L"Begin iterating " << p.wstring() << endl;  
    for (const auto& entry : directory_iterator{ p })  
    {  
        if (is_regular_file(entry.status()))  
        {  
            wcout << L" File: " << entry.path().filename() << " : "  
                << LastWriteTimeToLocalTime(entry.path());  
        }  
        else if (is_directory(entry.status()))  
        {  
            wcout << L" Dir: " << entry.path().filename() << endl;  
        }  
    }  
}  
  
void main()  
{  
    wstring dir{ LR"(C:\users\public\documents\)" };  
    path p{ dir };  
  
    if (!is_directory(p))  
    {  
        wcout << L"No such directory: " << dir << endl;  
        return;  
    }  
  
    DisplayFolderContents(p);  
    // IterateFolderRecursively(p); // see example   
  
    wcout << endl << L"Press Enter to exit" << endl;  
    wstring input;  
    getline(wcin, input);  
}  
```  
  
### Iterating a directory tree recursively  
 The following example shows how to iterate recursively through a directory tree. To run this function, paste it into the previous code example after the DisplayFolderContents function, and uncomment the line that calls it in main.  
  
```cpp  
// List files and directories recursively in the path  
void IterateFolderRecursively(const path& p)  
{  
    wcout << L"Begin iterating " << p.wstring() <<  
        " recursively" << endl;  
    for (recursive_directory_iterator it{ p }, end; it != end; ++it)  
    {  
        if (is_regular_file(it->status()))  
        {  
            wcout << setw(it.depth()) << L" " << L"File: " <<  
                it->path().filename() << L" : " <<  
                LastWriteTimeToLocalTime(it->path());  
        }  
        else if (is_directory(it->status()))  
        {  
            wcout << setw(it.depth()) << L" " << L"Dir: " <<  
                it->path().filename() << endl;  
        }  
    }  
}  
```  
  
### Handling symbolic links  
 Symbolic link detection is not yet supported in Visual C++ as of Visual Studio 2015.