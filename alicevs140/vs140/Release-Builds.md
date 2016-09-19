---
title: "Release Builds"
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
ms.assetid: fa9a78fa-f4b5-4722-baf4-aec655c4ff0f
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Release Builds
A release build uses optimizations. When you use optimizations to create a release build, the compiler will not produce symbolic debugging information. The absence of symbolic debugging information, along with the fact that code is not generated for TRACE and ASSERT calls, means that the size of your executable file is reduced and will therefore be faster.  
  
 This section presents information on why and when you would want to change from a debug build to a release build. It also discusses some of the problems you may encounter when changing from a debug to a release build:  
  
-   [Creating a Release Build](../vs140/How-to--Create-a-Release-Build.md)  
  
-   [Common Problems When Creating a Release Build](../vs140/Common-Problems-When-Creating-a-Release-Build.md)  
  
-   [Fixing Release Build Problems](../vs140/Fixing-Release-Build-Problems.md)  
  
    -   [Examining ASSERT Statements](../vs140/Using-VERIFY-Instead-of-ASSERT.md)  
  
    -   [Using the Debug Build To Check for Memory Overwrite](../vs140/Using-the-Debug-Build-to-Check-for-Memory-Overwrite.md)  
  
    -   [Debugging a Release Build](../vs140/How-to--Debug-a-Release-Build.md)  
  
    -   [Checking for Memory Overwrites](../vs140/Checking-for-Memory-Overwrites.md)  
  
## See Also  
 [Building C++ Projects in Visual Studio](../vs140/Building-C---Projects-in-Visual-Studio.md)   
 [C/C++ Building Reference](../vs140/C-C---Building-Reference.md)