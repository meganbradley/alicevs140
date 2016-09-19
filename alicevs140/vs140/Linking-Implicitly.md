---
title: "Linking Implicitly"
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
ms.assetid: 3ea4c316-4e70-4111-9944-c1b4ad00c605
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Linking Implicitly
To implicitly link to a DLL, executables must obtain the following from the provider of the DLL:  
  
-   A header file (.h file) containing the declarations of the exported functions and/or C++ classes.  The classes, functions, and data should all have `__declspec(dllimport)`, for more information, see [dllexport, dllimport](../vs140/dllexport--dllimport.md).  
  
-   An import library ([.LIB files](../vs140/.Lib-Files-as-Linker-Input.md)) to link with. (The linker creates the import library when the DLL is built.)  
  
-   The actual DLL (.dll file).  
  
 Executables using the DLL must include the header file containing the exported functions (or C++ classes) in each source file that contains calls to the exported functions. From a coding perspective, the function calls to the exported functions are just like any other function call.  
  
 To build the calling executable file, you must link with the import library. If you are using an external makefile, specify the file name of the import library where you list other object (.obj) files or libraries that you are linking with.  
  
 The operating system must be able to locate the DLL file when it loads the calling executable.  
  
## What do you want to do?  
  
-   [Link explicitly](../vs140/Linking-Explicitly.md)  
  
-   [Determine which linking method to use](../vs140/Determining-Which-Linking-Method-to-Use.md)  
  
## What do you want to know more about?  
  
-   [Working with Import Libraries and Export Files](../vs140/Working-with-Import-Libraries-and-Export-Files.md)  
  
-   [The search path used by Windows to locate a DLL](../vs140/Search-Path-Used-by-Windows-to-Locate-a-DLL.md)  
  
## See Also  
 [Linking an Executable to a DLL](../vs140/Linking-an-Executable-to-a-DLL.md)