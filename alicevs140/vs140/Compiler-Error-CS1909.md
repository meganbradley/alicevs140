---
title: "Compiler Error CS1909"
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
ms.assetid: d465a107-0911-4440-8b3a-1e5dea6fda3c
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1909
The DefaultValue attribute is not applicable on parameters of type 'type'  
  
 CS1909 is generated when you use a `DefaultValue` attribute that is not applicable on the parameter type.  
  
## Example  
 The following sample generates CS1909.  
  
```  
// CS1909.cs  
// compile with: /target:library  
using System.Runtime.InteropServices;  
  
public interface ISomeInterface  
{  
   void Test1([DefaultParameterValue(new int[] {1, 2})] int[] arr1);   // CS1909  
  
   void Test2([DefaultParameterValue("Test String")] string s);   // OK  
}  
```