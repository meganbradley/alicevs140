---
title: "Modifying WINVER and _WIN32_WINNT"
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
ms.assetid: 6a1f1d66-ae0e-48a7-81c3-524d8e8f3447
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Modifying WINVER and _WIN32_WINNT
Visual C++ no longer supports targeting Windows 95, Windows 98, Windows ME, Windows NT or Windows 2000. If your **WINVER** or **_WIN32_WINNT** macros are assigned to one of these versions of Windows, you must modify the macros. When you upgrade a project that was created by using an earlier version of Visual C++, you may see compilation errors related to the **WINVER** or **_WIN32_WINNT** macros if they are assigned to a version of Windows that is no longer supported.  
  
## Remarks  
 To modify the macros, in a header file (for example, targetver.h which is included when you create a project that targets Windows), add the following lines.  
  
```  
#define WINVER 0x0A00  
#define _WIN32_WINNT 0x0A00  
```  
  
 This targets the Windows 10 operating system. These values are listed in the Windows header file SDKDDKVer.h, which also defines macros for each Windows version. You should add the #define statement before including SDKDDKVer.h. Here are the lines from the Windows 10 version of SDKDDKVer.h that encode the values for each version of Windows:  
  
```  
//  
// _WIN32_WINNT version constants  
//  
#define _WIN32_WINNT_NT4                    0x0400 // Windows NT 4.0  
#define _WIN32_WINNT_WIN2K                  0x0500 // Windows 2000  
#define _WIN32_WINNT_WINXP                  0x0501 // Windows XP  
#define _WIN32_WINNT_WS03                   0x0502 // Windows Server 2003  
#define _WIN32_WINNT_WIN6                   0x0600 // Windows Vista  
#define _WIN32_WINNT_VISTA                  0x0600 // Windows Vista  
#define _WIN32_WINNT_WS08                   0x0600 // Windows Server 2008  
#define _WIN32_WINNT_LONGHORN               0x0600 // Windows Vista  
#define _WIN32_WINNT_WIN7                   0x0601 // Windows 7  
#define _WIN32_WINNT_WIN8                   0x0602 // Windows 8  
#define _WIN32_WINNT_WINBLUE                0x0603 // Windows 8.1  
#define _WIN32_WINNT_WINTHRESHOLD           0x0A00 // Windows 10  
#define _WIN32_WINNT_WIN10                  0x0A00 // Windows 10  
```  
  
 If you don't see all of these versions of Windows listed in a copy of SDKDDKVer.h that you're looking at, you probably are using an older version of the Windows SDK. By default, Win32 projects in [!INCLUDE[vs_dev14](../vs140/includes/vs_dev14_md.md)] use the Windows 8.1 SDK. To use the Windows 10 SDK, see [How to: Use the Windows 10 SDK](../vs140/How-to--Use-the-Windows-10-SDK-in-a-Windows-Desktop-Application.md).  
  
> [!NOTE]
>  Values are not guaranteed to work if you include internal MFC headers in your application.  
  
 You can also define this macro by using the **/D** compiler option. For more information, see [/D (Preprocessor Definitions)](../Topic/-D%20\(Preprocessor%20Definitions\).md).  
  
 For more information about the meanings of these macros, see [Using the Windows Headers](http://msdn.microsoft.com/library/windows/desktop/aa383745).  
  
## See Also  
 [Previous Product Changes](assetId:///91fa1713-0778-4b6b-82f7-0fe0a23ab1db)