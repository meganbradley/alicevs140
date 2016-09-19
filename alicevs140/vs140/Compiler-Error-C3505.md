---
title: "Compiler Error C3505"
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
ms.assetid: ed73c99e-93a1-4f3a-bac7-ba7ed5d836e4
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3505
cannot load type library 'guid'  
  
 C3505 can be caused if you are running the (32-bit to) 64-bit cross-compiler on a 64-bit machine because the compiler is running under WOW64 and can only read from the 32-bit registry hive.  
  
 You can resolve this C3505 by building 32-bit and 64-bit versions of the type library you are trying to import and register them both.  Or you can use the native 64-bit compiler, but that would require changing your VC++ Directories in the IDE to point to the 64-bit compiler.  
  
 For more information, see,  
  
-   [How to: Enable a 64-Bit Visual C++ Toolset at the Command Line](../vs140/How-to--Enable-a-64-Bit-Visual-C---Toolset-on-the-Command-Line.md)  
  
-   [How to: Use the 64-Bit C++ Command-line Tools](../vs140/How-to--Enable-a-64-Bit-Visual-C---Toolset-on-the-Command-Line.md)  
  
-   [How to: Configure Projects to Target 64-Bit Platforms](../vs140/How-to--Configure-Visual-C---Projects-to-Target-64-Bit-Platforms.md)