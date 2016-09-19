---
title: "Compiler Error CS0132"
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
ms.assetid: e8ad1281-2912-4b6a-b2af-a319a23ddd16
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0132
'constructor' : a static constructor must be parameterless  
  
 A [static](../vs140/static--C#-Reference-.md) constructor cannot be declared with one or more parameters. For more information, see [Constructors (C# Programmer's Reference)](../vs140/Constructors--C#-Programming-Guide-.md).  
  
 The following sample generates CS0132:  
  
```  
// CS0132.cs  
namespace MyNamespace  
{  
   public class MyClass  
   {  
      public MyClass(int i)  
      {  
      }  
   }  
  
   public class MyClass2 : MyClass  
   {  
      static MyClass2(int i)   // CS0132  
      {  
      }  
   }  
}  
```