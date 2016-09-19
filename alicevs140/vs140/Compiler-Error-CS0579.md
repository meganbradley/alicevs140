---
title: "Compiler Error CS0579"
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
ms.topic: error-reference
ms.assetid: 1a15af7e-60ad-4418-a493-15fdfe08e7db
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0579
Duplicate 'attribute' attribute  
  
 It is not possible to specify the same attribute more than once unless the attribute specifies **AllowMultiple=true** in its [AttributeUsage](../vs140/AttributeUsage--C#-and-Visual-Basic-.md).  
  
## Example  
 The following example generates CS0579.  
  
```c#  
// CS0579.cs  
using System;  
public class MyAttribute : Attribute  
{  
}  
  
[AttributeUsage(AttributeTargets.All,AllowMultiple=true)]  
public class MyAttribute2 : Attribute  
{  
}  
  
public class z  
{  
    [MyAttribute, MyAttribute]     // CS0579  
    public void zz()  
    {  
    }  
  
    [MyAttribute2, MyAttribute2]   // OK  
    public void zzz()  
    {  
    }  
  
    public static void Main()  
    {  
    }  
}  
```