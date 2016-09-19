---
title: "Compiler Warning (level 1) C4274"
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
ms.assetid: 5a948680-7ed1-469f-978d-ae99d154e161
caps.latest.revision: 15
---
# Compiler Warning (level 1) C4274
\#ident ignored; see documentation for #pragma comment(exestr, 'string')  
  
 The `#ident` directive, which inserts a user-specified string in the object or executable file, is deprecated. Consequently, the compiler ignores the directive.  
  
> [!CAUTION]
>  Warning C4274 advises you to use the [#pragma comment(exestr, 'string')](../vs140/comment--C-C---.md) directive. However, this advice is deprecated and will be revised in a future release of the compiler. If you use the `#pragma` directive, the linker tool (LINK.exe) ignores the comment record produced by the directive and issues warning [LNK4229](../vs140/Linker-Tools-Warning-LNK4229.md). Instead of the `#ident` directive, we recommend that you use a [file version resource string](_win32_Version_Information) in your application.  
  
### To correct this error  
  
-   Remove the `#ident "`*string*`"` directive.  
  
## See Also  
 [comment (C/C++)](../vs140/comment--C-C---.md)   
 [Linker Tools Warning LNK4229](../vs140/Linker-Tools-Warning-LNK4229.md)   
 [Version Information](_win32_Version_Information)   
 [Working with Resource Files](../vs140/Working-with-Resource-Files.md)