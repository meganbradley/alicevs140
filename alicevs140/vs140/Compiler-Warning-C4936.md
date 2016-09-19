---
title: "Compiler Warning C4936"
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
ms.assetid: 6676de35-bf1b-4d0b-a70f-b5734130336c
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning C4936
this __declspec is supported only when compiled with /clr or /clr:pure  
  
 A `__declspec` modifier was used but that `__declspec` modifier is only valid when compiled with one of the [/clr](../Topic/-clr%20\(Common%20Language%20Runtime%20Compilation\).md) options.  
  
 For more information, see [appdomain](../vs140/appdomain.md) and [process](../vs140/process.md).  
  
 C4936 is always issued as an error.  You can disable C4936 with the [warning](../vs140/warning.md) pragma.  
  
 The following sample generates C4936:  
  
```  
// C4936.cpp  
// compile with: /c  
// #pragma warning (disable : 4936)  
__declspec(process) int i;   // C4936  
__declspec(appdomain) int j;   // C4936  
```