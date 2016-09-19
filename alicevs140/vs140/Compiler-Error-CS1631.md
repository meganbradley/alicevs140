---
title: "Compiler Error CS1631"
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
ms.assetid: bf0c5ff9-90a3-4db6-b4ee-0b93e31614e0
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1631
Cannot yield a value in the body of a catch clause  
  
 The yield statement is not allowed from within the body of a catch clause. To avoid this error, move the yield statement outside the body of the catch clause.  
  
 The following sample generates CS1631:  
  
```  
// CS1631.cs  
using System;  
using System.Collections;  
  
public class C : IEnumerable  
{  
   public IEnumerator GetEnumerator()   
   {  
      try  
      {  
      }  
      catch(Exception e)  
      {  
        yield return this;  // CS1631  
      }  
   }    
  
   public static void Main()   
   {  
   }  
}  
```