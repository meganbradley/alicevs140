---
title: "Compiler Error CS0175"
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
ms.assetid: cedd769d-8258-4235-a321-362981b9f84b
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0175
Use of keyword 'base' is not valid in this context  
  
 The [base](../vs140/base--C#-Reference-.md) keyword must be used to specify a particular member of the base class. For more information, see [Constructors (C# Programmer's Reference)](../vs140/Constructors--C#-Programming-Guide-.md).  
  
 The following sample generates CS0175:  
  
```  
// CS0175.cs  
using System;  
class BaseClass  
{  
    public int TestInt = 0;  
}  
  
class MyClass : BaseClass  
{  
    public static void Main()  
    {  
        MyClass aClass = new MyClass();  
        aClass.BaseTest();  
    }  
  
    public void BaseTest()  
    {  
        Console.WriteLine(base); // CS0175  
        // Try the following line instead:  
        // Console.WriteLine(base.TestInt);  
        base = 9;   // CS0175  
  
        // Try the following line instead:  
        // base.TestInt = 9;  
    }  
}  
```