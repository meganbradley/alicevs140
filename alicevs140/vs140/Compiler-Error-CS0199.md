---
title: "Compiler Error CS0199"
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
ms.assetid: 9eede3f2-b55a-4b85-a05d-6bf177e1c602
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0199
Fields of static readonly field 'name' cannot be passed ref or out (except in a static constructor)  
  
 A [readonly](../vs140/readonly--C#-Reference-.md) variable must have the same [static](../vs140/static--C#-Reference-.md) usage as the constructor in which you want to pass it as a [ref](../vs140/ref--C#-Reference-.md) or [out](../vs140/out--C#-Reference-.md) parameter. For more information, see [Passing Parameters (C# Programmer's Reference)](../vs140/Passing-Parameters--C#-Programming-Guide-.md).  
  
## Example  
 The following sample generates CS0199:  
  
```  
// CS0199.cs  
class MyClass  
{  
    public static readonly int TestInt = 6;  
  
    static void TestMethod(ref int testInt)  
    {  
        testInt = 0;  
    }  
  
    MyClass()  
    {  
        TestMethod(ref TestInt);   // CS0199, TestInt is static  
    }  
  
    public static void Main()  
    {  
    }  
}  
```