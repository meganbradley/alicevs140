---
title: "Creating Precompiled Header Files"
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
ms.assetid: e2cdb404-a517-4189-9771-c869c660cb1b
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Creating Precompiled Header Files
The Microsoft C and C++ compilers provide options for precompiling any C or C++ code, including inline code. Using this performance feature, you can compile a stable body of code, store the compiled state of the code in a file, and, during subsequent compilations, combine the precompiled code with code that is still under development. Each subsequent compilation is faster because the stable code does not need to be recompiled.  
  
 This section covers the following precompiled header issues:  
  
-   [When to Precompile Source Code](../vs140/When-to-Precompile-Source-Code.md)  
  
-   [Two Choices for Precompiling Code](../vs140/Two-Choices-for-Precompiling-Code.md)  
  
-   [Precompiled Header Consistency Rules](../vs140/Precompiled-Header-Consistency-Rules.md)  
  
-   [Using Precompiled Headers in a Project](../vs140/Using-Precompiled-Headers-in-a-Project.md)  
  
 For reference information on the compiler options related to precompiled headers, see [/Y (Precompiled Headers)](../vs140/-Y--Precompiled-Headers-.md).  
  
## See Also  
 [C/C++ Building Reference](../vs140/C-C---Building-Reference.md)   
 [Compiler Options](../vs140/Compiler-Options.md)