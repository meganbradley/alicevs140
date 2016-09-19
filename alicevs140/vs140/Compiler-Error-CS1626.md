---
title: "Compiler Error CS1626"
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
ms.assetid: 3ba03383-eb24-4fd8-bf40-8b0f7d6baf0d
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1626
Cannot yield a value in the body of a try block with a catch clause  
  
 A yield statement is not allowed in a try block if there is a catch clause associated with the try block. To avoid this error, move the yield statement out of the catch clause.  
  
 The following sample generates CS1626:  
  
```  
// CS1626.cs  
using System.Collections;  
  
class C : IEnumerable  
{  
   public IEnumerator GetEnumerator()  
   {  
      try  
      {  
         yield return this;  // CS1626  
      }  
      catch  
      {  
  
      }  
   }  
}  
  
public class CMain  
{  
   public static void Main() { }  
}  
  
```