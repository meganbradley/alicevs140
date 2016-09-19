---
title: "Compiler Error CS1641"
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
ms.assetid: ba6eab47-c28b-4531-b6a0-6d538b236d19
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1641
A fixed size buffer field must have the array size specifier after the field name  
  
 Unlike regular arrays, fixed size buffers require a constant size to be specified at the declaration point. To resolve this error, add a positive integer literal or a constant positive integer and put the square brackets after the identifier.  
  
 The following sample generates CS1641:  
  
```  
// CS1641.cs  
// compile with: /unsafe /target:library  
unsafe struct S {  
   fixed int [] a;  // CS1641  
  
   // OK  
   fixed int b [10];  
   const int c = 10;  
   fixed int d [c];  
}  
```