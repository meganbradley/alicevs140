---
title: "Compiler Error CS0592"
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
ms.topic: error-reference
ms.assetid: 805c8cf0-eca2-4040-badd-a9c09ab5c747
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0592
Attribute 'attribute' is not valid on this declaration type. It is valid on 'type' declarations only.  
  
 When you define an attribute, you define what constructs it can be applied to by specifying an `AttributeTargets` value. In the following example, the `MyAttribute` attribute can be applied to interfaces only, because the `AttributeUsage` attribute specifies `AttributeTargets.Iterface`. The error is generated because the attribute is applied to a class (class `A`).  
  
## Example  
 The following sample generates CS0592:  
  
```  
// CS0592.cs  
using System;  
  
[AttributeUsage(AttributeTargets.Interface)]  
public class MyAttribute : Attribute   
{  
}  
  
[MyAttribute]  
// Generates CS0592 because MyAttribute is not valid for a class.   
public class A    
{  
    public static void Main()  
    {  
    }  
}  
```  
  
## See Also  
 [Attributes (C# Programming Guide)](../vs140/Attributes--C#-and-Visual-Basic-.md)