---
title: "Troubleshooting IntelliSense in C++ Projects"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 72e4eb39-66d3-403d-8da7-00ed288a1899
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Troubleshooting IntelliSense in C++ Projects
IntelliSense can stop working under certain conditions. Use the following steps to help determine why IntelliSense does not work for C++ projects.  
  
### To investigate IntelliSense failure in C++ projects  
  
1.  Make sure that the Visual C++ project contains no compilation errors.  
  
    1.  If the project is a Makefile project, see [How to: Enable IntelliSense for Makefile Projects](../vs140/How-to--Enable-IntelliSense-for-Makefile-Projects.md).  
  
2.  Make sure that stdafx.h is on the include path. For more information about include paths in Visual C++ projects, see [#include](../vs140/#include-Directive--C-C---.md) and [/I](../vs140/-I--Additional-Include-Directories-.md).  
  
## IntelliSense Limitations  
 IntelliSense does not work in C++ projects under the following circumstances:  
  
-   The cursor is in a code comment.  
  
-   You are writing a string literal.  
  
-   A syntax error appears over the cursor.  
  
-   The solution consists of either the syntax for managed C++, or the earlier Managed Extensions for C++ syntax.  
  
-   IntelliSense is not fully supported when you reference a header file multiple times by using the `#include` directive, and the meaning of that header file changes because of various macro states that are defined through the `#define` directive. In other words, when you include a header file several times and the header usage changes under different macro states, IntelliSense does not always work.  
  
## See Also  
 [Troubleshooting IntelliSense](assetId:///c1b3adb9-0d48-4770-a51e-392ed818c484)   
 [How to: Organize Project Output Files for Builds](../vs140/How-to--Organize-Project-Output-Files-for-Builds.md)