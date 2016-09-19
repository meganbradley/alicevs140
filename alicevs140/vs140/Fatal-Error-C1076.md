---
title: "Fatal Error C1076"
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
ms.topic: error-reference
ms.assetid: 84ac1180-3e8a-48e8-9f77-7f18a778b964
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Fatal Error C1076
compiler limit : internal heap limit reached; use /Zm to specify a higher limit  
  
 This error can be caused by too many symbols, or too many template instantiations.  
  
 To resolve this error:  
  
1.  Use the [/Zm](../Topic/-Zm%20\(Specify%20Precompiled%20Header%20Memory%20Allocation%20Limit\).md) option to set the compiler memory limit to the value specified in the [C3859](../vs140/Compiler-Error-C3859.md) error message. For more information that includes how to set this value in [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)], see the Remarks section in [/Zm (Specify Precompiled Header Memory Allocation Limit)](../Topic/-Zm%20\(Specify%20Precompiled%20Header%20Memory%20Allocation%20Limit\).md).  
  
2.  If you are using the 32-bit hosted compilers on a 64-bit operating system, use the 64-bit hosted compilers instead. For more information, see [How to: Enable a 64-Bit Visual C++ Toolset on the Command Line](../vs140/How-to--Enable-a-64-Bit-Visual-C---Toolset-on-the-Command-Line.md).  
  
3.  Eliminate unnecessary include files.  
  
4.  Eliminate unnecessary global variables—for example, by allocating memory dynamically instead of declaring a large array.  
  
5.  Eliminate unused declarations.  
  
6.  Split large functions into smaller functions.  
  
7.  Split large classes into smaller classes.  
  
8.  Split the current file into smaller files.  
  
 If C1076 occurs immediately after the build starts, the value specified for **/Zm** is probably too high for your program. Reduce the **/Zm** value.