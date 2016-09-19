---
title: "When to Precompile Source Code"
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
ms.assetid: eb8ba193-fd87-40d3-9545-c75deabe37cb
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# When to Precompile Source Code
Precompiled code is useful during the development cycle to reduce compilation time, especially if:  
  
-   You always use a large body of code that changes infrequently.  
  
-   Your program comprises multiple modules, all of which use a standard set of include files and the same compilation options. In this case, all include files can be precompiled into one precompiled header.  
  
 The first compilation — the one that creates the precompiled header file — takes a bit longer than subsequent compilations. Subsequent compilations can proceed more quickly by including the precompiled code.  
  
 You can precompile both C and C++ programs. In C++ programming, it is common practice to separate class interface information into header files. These header files can later be included in programs that use the class. By precompiling these headers, you can reduce the time a program takes to compile.  
  
> [!NOTE]
>  Although you can use only one precompiled header (.pch) file per source file, you can use multiple .pch files in a project.  
  
## See Also  
 [Creating Precompiled Header Files](../vs140/Creating-Precompiled-Header-Files.md)