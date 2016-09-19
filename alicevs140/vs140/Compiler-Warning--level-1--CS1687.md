---
title: "Compiler Warning (level 1) CS1687"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f65d184f-fa1d-45d7-be7d-f439f67bace4
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) CS1687
Source file has exceeded the limit of 16,707,565 lines representable in the PDB, debug information will be incorrect  
  
 The PDB and debugger have some limitations about how big a file can be. If the source file is too big, the debugger will not behave properly beyond that limit. The user should either not emit debug information for that file by possibly using `#line hidden`, or they should find a way to shrink the file, possibly by splitting the file into multiple files. They might want to use the `partial` keyword to split up a large class.