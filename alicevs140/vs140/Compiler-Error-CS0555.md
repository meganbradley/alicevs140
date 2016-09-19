---
title: "Compiler Error CS0555"
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
ms.assetid: e4b2f890-98b4-4578-b1de-ebaafc8b3da2
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0555
User-defined operator cannot take an object of the enclosing type and convert to an object of the enclosing type  
  
 User-defined conversions to values of the enclosing class are not allowed; you do not need such an operator.  
  
 The fo3llowing sample generates CS0555:  
  
```  
// CS0555.cs  
public class MyClass  
{  
   // delete the following operator to resolve this CS0555  
   public static implicit operator MyClass(MyClass aa)   // CS0555  
   {  
      return new MyClass();  
   }  
  
   public static void Main()  
   {  
   }  
}  
```