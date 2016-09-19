---
title: "Compiler Error CS0715"
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
ms.assetid: e3cd1e46-ccfa-4678-a2ed-69245f3558ba
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0715
'static class' : static classes cannot contain user defined operators  
  
 User defined operators operate on instances of classes. Static classes cannot be instantiated, so it is not possible to create instances for operators to act upon. Hence, user defined operators are not allowed for static classes.  
  
 The following sample generates CS0715:  
  
```  
// CS0715.cs  
public static class C  
{  
   public static C operator+(C c)  // CS0715  
   {  
   }  
  
   public static void Main()  
   {  
   }  
}  
```