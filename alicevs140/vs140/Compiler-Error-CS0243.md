---
title: "Compiler Error CS0243"
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
ms.assetid: 2506e4cb-dc26-46b4-a58c-ab6bf1601144
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0243
The Conditional attribute is not valid on 'method' because it is an override method  
  
 The [Conditional](assetId:///e1c4913b-74d0-421a-8a6d-c14b3f0e68fb) attribute is not allowed on a method that is marked with the [override](../vs140/override--C#-Reference-.md) keyword. For more information, see [Knowing When to Use Override and New Keywords (C# Programmer's Reference)](../vs140/Knowing-When-to-Use-Override-and-New-Keywords--C#-Programming-Guide-.md).  
  
 The compiler never binds to override methods; it only binds to the base method and the common language runtime calls the override, as appropriate.  
  
 The following sample generates CS0243:  
  
```  
// CS0243.cs  
// compile with: /target:library  
public class MyClass  
{  
   public virtual void M() {}  
}  
  
public class MyClass2 : MyClass  
{  
   [System.Diagnostics.ConditionalAttribute("MySymbol")]   // CS0243  
   // remove Conditional attribute or remove override keyword  
   public override void M() {}  
}  
```