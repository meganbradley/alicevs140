---
title: "Compiler Error CS0192"
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
ms.assetid: d3fb6d18-dbf3-42c3-a280-afe55b97c2d1
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0192
Fields of static readonly field 'name' cannot be passed ref or out (except in a static constructor)  
  
 A field (variable) marked with the [readonly](../vs140/readonly--C#-Reference-.md) keyword cannot be passed either to a [ref](../vs140/ref--C#-Reference-.md) or [out](../vs140/out--C#-Reference-.md) parameter except inside a constructor. For more information, see [Properties and Fields (C# Programmer's Reference)](../vs140/Fields--C#-Programming-Guide-.md).  
  
 CS0192 also results if the `readonly` field is [static](../vs140/static--C#-Reference-.md) and the constructor is not marked `static`.  
  
## Example  
 The following sample generates CS0192.  
  
```  
// CS0192.cs  
class MyClass  
{  
    public readonly int TestInt = 6;  
    static void TestMethod(ref int testInt)  
    {  
        testInt = 0;  
    }  
  
    MyClass()  
    {  
        TestMethod(ref TestInt);   // OK  
    }  
  
    public void PassReadOnlyRef()  
    {  
        TestMethod(ref TestInt);   // CS0192  
    }  
  
    public static void Main()  
    {  
    }  
}  
```