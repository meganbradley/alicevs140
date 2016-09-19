---
title: "Compiler Error CS0564"
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
ms.assetid: 4c152e10-eb22-4437-a85f-1599c76470e0
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0564
The first operand of an overloaded shift operator must have the same type as the containing type, and the type of the second operand must be int  
  
 You attempted to overload a shift operator (<< or >>) with incorrectly typed operands. The first operand must be the type and the second operand must be of the type `int`.  
  
 The following sample generates CS0564:  
  
```  
// CS0564.cs  
using System;  
class C  
{  
   public static int operator << (C c1, C c2) // CS0564  
// To correct, change second operand to int, like so:  
// public static int operator << (C c1, int c2)  
   {  
      return 0;  
   }  
   static void Main()   
   {  
   }  
}  
```