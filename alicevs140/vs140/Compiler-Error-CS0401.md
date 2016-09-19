---
title: "Compiler Error CS0401"
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
ms.assetid: 94eac5a8-7344-44d2-9d0c-a9954993603d
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0401
The new() constraint must be the last constraint specified  
  
 When using multiple constraints, list all other constraints before the new() constraint.  
  
## Example  
 The following sample generates CS0401.  
  
```  
// CS0401.cs  
// compile with: /target:library  
using System;  
 class C<T> where T : new(), IDisposable {}  // CS0401  
  
class D<T> where T : IDisposable  
{  
   static void F<U>() where U : new(), IDisposable{}   // CS0401  
}  
```