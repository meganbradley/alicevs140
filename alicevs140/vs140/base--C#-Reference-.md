---
title: "base (C# Reference)"
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
ms.assetid: 8b645dbe-1a33-49b8-8716-1c401f9a5ea5
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# base (C# Reference)
The `base` keyword is used to access members of the base class from within a derived class:  
  
-   Call a method on the base class that has been overridden by another method.  
  
-   Specify which base-class constructor should be called when creating instances of the derived class.  
  
 A base class access is permitted only in a constructor, an instance method, or an instance property accessor.  
  
 It is an error to use the `base` keyword from within a static method.  
  
 The base class that is accessed is the base class specified in the class declaration. For example, if you specify `class ClassB : ClassA`, the members of ClassA are accessed from ClassB, regardless of the base class of ClassA.  
  
## Example  
 In this example, both the base class, `Person`, and the derived class, `Employee`, have a method named `Getinfo`. By using the `base` keyword, it is possible to call the `Getinfo` method on the base class, from within the derived class.  
  
 [!CODE [csrefKeywordsAccess#1](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsAccess#1)]  
  
 For additional examples, see [new](../vs140/new--C#-Reference-.md), [virtual](../vs140/virtual--C#-Reference-.md), and [override](../vs140/override--C#-Reference-.md).  
  
## Example  
 This example shows how to specify the base-class constructor called when creating instances of a derived class.  
  
 [!CODE [csrefKeywordsAccess#2](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsAccess#2)]  
  
## C# Language Specification  
 [!INCLUDE[CSharplangspec](../vs140/includes/Csharplangspec_md.md)]  
  
## See Also  
 [C# Reference](../vs140/C#-Reference.md)   
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [C# Keywords](../Topic/C%23%20Keywords.md)   
 [this](../vs140/this--C#-Reference-.md)