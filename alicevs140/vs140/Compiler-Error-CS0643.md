---
title: "Compiler Error CS0643"
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
ms.assetid: beae30ff-15c2-413f-8f5c-504cdba2e57a
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0643
'arg' duplicate named attribute argument  
  
 A parameter, `arg`, on a user-defined attribute was specified twice. For more information, see [Attributes (C# Programmers Reference)](../vs140/Attributes--C#-and-Visual-Basic-.md).  
  
## Example  
 The following sample generates CS0643:  
  
```  
// CS0643.cs  
using System;  
using System.Runtime.InteropServices;  
  
[AttributeUsage(AttributeTargets.Class)]  
public class MyAttribute : Attribute  
{  
    public MyAttribute()  
    {  
    }  
  
    public int x;  
}  
  
[MyAttribute(x = 5, x = 6)]   // CS0643, error setting x twice  
// try the following line instead  
// [MyAttribute(x = 5)]  
class MyClass  
{  
}  
  
public class MainClass  
{  
    public static void Main ()  
    {  
    }  
}  
```