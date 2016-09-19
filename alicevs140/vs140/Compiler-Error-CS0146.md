---
title: "Compiler Error CS0146"
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
ms.assetid: 2be796e5-da2c-4939-af12-3145cd1828c8
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0146
Circular base class dependency involving 'class1' and 'class2'  
  
 The inheritance list for a class includes a direct or indirect reference to itself. A class cannot inherit from itself. For more information, see [Inheritance (C# Programmer's Reference)](../Topic/Inheritance%20\(C%23%20Programming%20Guide\).md).  
  
 The following sample generates CS0146:  
  
```  
// CS0146.cs  
namespace MyNamespace  
{  
   public interface InterfaceA  
   {  
   }  
  
   public class MyClass : InterfaceA, MyClass2  
   {  
      public void Main()  
      {  
      }  
   }  
  
   public class MyClass2 : MyClass   // CS0146  
   {  
   }  
}  
```