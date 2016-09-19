---
title: "Compiler Error CS0549"
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
ms.assetid: ae965019-9dee-4f28-9e9a-6f379bd0d757
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0549
'function' is a new virtual member in sealed class 'class'  
  
 A [sealed](../vs140/sealed--C#-Reference-.md)[class](../vs140/class--C#-Reference-.md) cannot be used as a base class.  Therefore, it is useless to have a virtual method in sealed class.  
  
 The following sample generates CS0549:  
  
```  
// CS0549.cs  
// compile with: /target:library  
sealed public class MyClass  
{  
   virtual public void TestMethod() {}   // CS0549  
   public void TestMethod2() {}   // OK  
}  
```