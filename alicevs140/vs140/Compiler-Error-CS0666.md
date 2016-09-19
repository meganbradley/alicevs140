---
title: "Compiler Error CS0666"
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
ms.assetid: 44ad4574-b4a2-487b-8d05-0116762231ab
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0666
'member' : new protected member declared in struct  
  
 A [struct](../vs140/struct--C#-Reference-.md) cannot be [abstract](../vs140/abstract--C#-Reference-.md) and is always implicitly [sealed](../vs140/sealed--C#-Reference-.md). Because structs do not support inheritance, the concept of a [protected](../vs140/protected--C#-Reference-.md) member in a struct makes no sense. For more information, see [Inheritance (C# Programmer's Reference)](../Topic/Inheritance%20\(C%23%20Programming%20Guide\).md).  
  
## Example  
 The following sample generates CS0666:  
  
```  
// CS0666.cs  
class M  
{  
    static void Main()  
    {  
    }  
}  
  
struct S  
{  
    protected int x;   // CS0666  
}  
```