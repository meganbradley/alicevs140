---
title: "Object Expressions (F#)"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - FSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-fsharp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: c2b23aa3-63de-4bea-aa73-6b54fefb5252
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Object Expressions (F#)
An *object expression* is an expression that creates a new instance of a dynamically created, anonymous object type that is based on an existing base type, interface, or set of interfaces.  
  
## Syntax  
  
```  
// When typename is a class:  
{ new typename [type-params] arguments with  
   member-definitions  
  [ additional-interface-definitions ]  
}  
// When typename is not a class:  
{ new typename [generic-type-args] with  
   member-definitions  
  [ additional-interface-definitions ]  
}  
```  
  
## Remarks  
 In the previous syntax, the `typename` represents an existing class type or interface type. `type-params` describes the optional generic type parameters. The `arguments` are used only for class types, which require constructor parameters. The `member-definitions` are overrides of base class methods, or implementations of abstract methods from either a base class or an interface.  
  
 The following example illustrates several different types of object expressions.  
  
 [!CODE [FsLangRef2#4301](../CodeSnippet/VS_Snippets_Fsharp/fslangref2#4301)]  
  
## Using Object Expressions  
 You use object expressions when you want to avoid the extra code and overhead that is required to create a new, named type. If you use object expressions to minimize the number of types created in a program, you can reduce the number of lines of code and prevent the unnecessary proliferation of types. Instead of creating many types just to handle specific situations, you can use an object expression that customizes an existing type or provides an appropriate implementation of an interface for the specific case at hand.  
  
## See Also  
 [F# Language Reference](../Topic/F%23%20Language%20Reference.md)