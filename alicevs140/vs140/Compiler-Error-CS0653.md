---
title: "Compiler Error CS0653"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c94043b9-b5d9-4294-921d-a4aead124d44
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0653
Cannot apply attribute class 'class' because it is abstract  
  
 An [abstract](../vs140/abstract--C#-Reference-.md) custom attribute class cannot be used as an attribute.  
  
 The following sample generates CS0653:  
  
```  
// CS0653.cs  
using System;  
  
public abstract class MyAttribute : Attribute  
{  
}  
  
public class My2Attribute : MyAttribute  
{  
}  
  
[My]   // CS0653  
// try the following line instead  
// [My2]  
class MyClass  
{  
   public static void Main()  
   {  
   }  
}  
```