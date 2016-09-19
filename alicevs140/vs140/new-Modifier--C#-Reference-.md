---
title: "new Modifier (C# Reference)"
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
ms.assetid: a2e20856-33b9-4620-b535-a60dbce8349b
caps.latest.revision: 30
translation.priority.ht: 
  - de-de
  - ja-jp
---
# new Modifier (C# Reference)
When used as a declaration modifier, the `new` keyword explicitly hides a member that is inherited from a base class. When you hide an inherited member, the derived version of the member replaces the base class version. Although you can hide members without using the `new` modifier, you get a compiler warning. If you use `new` to explicitly hide a member, it suppresses this warning.  
  
 To hide an inherited member, declare it in the derived class by using the same member name, and modify it with the `new` keyword. For example:  
  
 [!CODE [csrefKeywordsOperator#8](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsOperator#8)]  
  
 In this example, `BaseC.Invoke` is hidden by `DerivedC.Invoke`. The field `x` is not affected because it is not hidden by a similar name.  
  
 Name hiding through inheritance takes one of the following forms:  
  
-   Generally, a constant, field, property, or type that is introduced in a class or struct hides all base class members that share its name.  There are special cases.  For example, if you declare a new field with name `N` to have a type that is not invocable, and a base type declares `N` to be a method, the new field does not hide the base declaration in invocation syntax.  See the [C# language specification](http://go.microsoft.com/fwlink/?LinkId=199552) for details (see section "Member Lookup" in section "Expressions").  
  
-   A method introduced in a class or struct hides properties, fields, and types that share that name in the base class. It also hides all base class methods that have the same signature.  
  
-   An indexer introduced in a class or struct hides all base class indexers that have the same signature.  
  
 It is an error to use both `new` and [override](../vs140/override--C#-Reference-.md) on the same member, because the two modifiers have mutually exclusive meanings. The `new` modifier creates a new member with the same name and causes the original member to become hidden. The `override` modifier extends the implementation for an inherited member.  
  
 Using the `new` modifier in a declaration that does not hide an inherited member generates a warning.  
  
## Example  
 In this example, a base class, `BaseC`, and a derived class, `DerivedC`, use the same field name `x`, which hides the value of the inherited field. The example demonstrates the use of the `new` modifier. It also demonstrates how to access the hidden members of the base class by using their fully qualified names.  
  
 [!CODE [csrefKeywordsOperator#9](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsOperator#9)]  
  
## Example  
 In this example, a nested class hides a class that has the same name in the base class. The example demonstrates how to use the `new` modifier to eliminate the warning message and how to access the hidden class members by using their fully qualified names.  
  
 [!CODE [csrefKeywordsOperator#10](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsOperator#10)]  
  
 If you remove the `new` modifier, the program will still compile and run, but you will get the following warning:  
  
```  
The keyword new is required on 'MyDerivedC.x' because it hides inherited member 'MyBaseC.x'.  
```  
  
## C# Language Specification  
 [!INCLUDE[CSharplangspec](../vs140/includes/Csharplangspec_md.md)]  
  
## See Also  
 [C# Reference](../vs140/C#-Reference.md)   
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [C# Keywords](../Topic/C%23%20Keywords.md)   
 [Operator Keywords](../vs140/Operator-Keywords--C#-Reference-.md)   
 [Modifiers](../vs140/Modifiers--C#-Reference-.md)   
 [Versioning with the Override and New Keywords](../vs140/Versioning-with-the-Override-and-New-Keywords--C#-Programming-Guide-.md)   
 [Knowing When to Use Override and New Keywords](../vs140/Knowing-When-to-Use-Override-and-New-Keywords--C#-Programming-Guide-.md)