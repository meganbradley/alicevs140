---
title: "Type &#39;&lt;typename&gt;&#39; has no type parameters and so cannot have type arguments"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b86e784c-6718-4585-bd39-2f0982068828
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Type &#39;&lt;typename&gt;&#39; has no type parameters and so cannot have type arguments
A declaration or assignment statement includes an [Of](../Topic/Of%20Clause%20\(Visual%20Basic\).md) clause when invoking a non-generic type.  
  
 By its definition, a *generic type* is a class, structure, interface, procedure, or delegate that operates on data types you can specify through one or more *type parameters*. When the using code creates a type from this generic type, it supplies a *type argument* to each type parameter. As part of the creation of the type, each type argument replaces every occurrence of its corresponding type parameter in the generated code.  
  
 Type parameters are defined with an `Of` clause inside parentheses, and type arguments are supplied using an `Of` clause inside parentheses. The `Of` clause is used only when dealing with generic types.  
  
 Non-generic types do not accept type parameters, and you cannot specify any type arguments when you invoke such a type.  
  
 **Error ID:** BC32045  
  
### To correct this error  
  
1.  Check the spelling of the type you are using in the declaration or assignment statement.  
  
2.  If you are invoking a non-generic type, remove the `Of` clause and its parentheses, if any. Do not remove parentheses surrounding a standard argument list for a procedure, delegate, or class constructor.  
  
## See Also  
 [Generic Types in Visual Basic](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)   
 [Type List](../vs140/Type-List--Visual-Basic-.md)   
 [How to: Use a Generic Class](../Topic/How%20to:%20Use%20a%20Generic%20Class%20\(Visual%20Basic\).md)