---
title: "Compiler Error CS0101"
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
ms.assetid: edb5246b-c16b-4845-bb2d-0ef769d014c7
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0101
The namespace 'namespace' already contains a definition for 'type'  
  
 A [namespace](../vs140/namespace--C#-Reference-.md) has duplicate identifiers. Rename or delete one of the duplicate identifiers. For more information, see [Namespaces (C# Programmer's Reference)](../vs140/Namespaces--C#-Programming-Guide-.md)  
  
 The following sample generates CS0101:  
  
```  
// CS0101.cs  
namespace MyNamespace  
{  
   public class MyClass  
   {  
      static public void Main()  
      {  
      }  
   }  
  
   public class MyClass   // CS0101  
   {  
   }  
}  
```