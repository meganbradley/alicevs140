---
title: "Compiler Error CS0191"
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
ms.assetid: 512479e4-656e-4dcb-8d71-801541d72dcd
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0191
Property or indexer 'name' cannot be assigned to -- it is read only  
  
 A [readonly](../vs140/readonly--C#-Reference-.md) field can only take an assignment in a constructor or at declaration. For more information, see [Constructors (C# Programmer's Reference)](../vs140/Constructors--C#-Programming-Guide-.md).  
  
 CS0191 also results if the `readonly` field is [static](../vs140/static--C#-Reference-.md) and the constructor is not marked `static`.  
  
## Example  
 The following sample generates CS0191.  
  
```  
// CS0191.cs  
class MyClass  
{  
    public readonly int TestInt = 6;  // OK to assign to readonly field in declaration  
  
    MyClass()  
    {  
        TestInt = 11; // OK to assign to readonly field in constructor  
    }  
  
    public void TestReadOnly()  
    {  
        TestInt = 19;                  // CS0191  
    }  
  
    public static void Main()  
    {  
    }  
}  
```