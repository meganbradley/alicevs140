---
title: "Automatic Linking of MFC Library Version"
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
ms.assetid: 02af4a20-2034-4fce-b200-c2202c3c8311
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Automatic Linking of MFC Library Version
In versions of MFC before version 3.0 (before Visual C++ version 2.0), you had to manually specify the correct version of the MFC library in the input list of libraries for the linker. With MFC version 3.0 and later, it is no longer necessary to manually specify the version of the MFC library. Instead, the MFC header files automatically determine the correct version of the MFC library, based on values defined with `#define`, such as **_DEBUG** or **_UNICODE**. The MFC header files add **/defaultlib** directives instructing the linker to link in a specific version of the MFC library.  
  
 For example, the following code fragment from the AFX.H header file instructs the linker to link in either the NAFXCWD.LIB or NAFXCW.LIB version of MFC, depending on whether you are using the debug version of MFC:  
  
 `#ifndef _UNICODE`  
  
 `#ifdef _DEBUG`  
  
 `#pragma comment(lib, "nafxcwd.lib")`  
  
 `#else`  
  
 `#pragma comment(lib, "nafxcw.lib")`  
  
 `#endif`  
  
 `#else`  
  
 `#ifdef _DEBUG`  
  
 `#pragma comment(lib, "uafxcwd.lib")`  
  
 `#else`  
  
 `#pragma comment(lib, "uafxcw.lib")`  
  
 `#endif`  
  
 `#endif`  
  
 MFC header files also link in all required libraries, including MFC libraries, Win32 libraries, OLE libraries, OLE libraries built from samples, ODBC libraries, and so on. The Win32 libraries include Kernel32.Lib, User32.Lib, and GDI32.Lib.  
  
## See Also  
 [MFC Library Versions](../vs140/MFC-Library-Versions.md)