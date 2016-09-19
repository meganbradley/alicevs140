---
title: "let Bindings in Classes (F#)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - FSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-fsharp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: a492df11-7701-4c02-ba30-45edbea9ab5c
caps.latest.revision: 25
translation.priority.ht: 
  - de-de
  - ja-jp
---
# let Bindings in Classes (F#)
You can define private fields and private functions for F# classes by using `let` bindings in the class definition.  
  
## Syntax  
  
```  
// Field.  
[static] let [ mutable ] binding1 [ and ... binding-n ]  
  
// Function.  
[static] let [ rec ] binding1 [ and ... binding-n ]  
```  
  
## Remarks  
 The previous syntax appears after the class heading and inheritance declarations but before any member definitions. The syntax is like that of `let` bindings outside of classes, but the names defined in a class have a scope that is limited to the class. A `let` binding creates a private field or function; to expose data or functions publicly, declare a property or a member method.  
  
 A `let` binding that is not static is called an instance `let` binding. Instance `let` bindings execute when objects are created. Static `let` bindings are part of the static initializer for the class, which is guaranteed to execute before the type is first used.  
  
 The code within instance `let` bindings can use the primary constructor's parameters.  
  
 Attributes and accessibility modifiers are not permitted on `let` bindings in classes.  
  
 The following code examples illustrate several types of `let` bindings in classes.  
  
 [!CODE [FsLangRef1#3001](../CodeSnippet/VS_Snippets_Fsharp/fslangref1#3001)]  
  
 The output is as follows.  
  
```  
10 52 1 204  
```  
  
## Alternative Ways to Create Fields  
 You can also use the `val` keyword to create a private field. When using the `val` keyword, the field is not given a value when the object is created, but instead is initialized with a default value. For more information, see [Fields: the val keyword](../Topic/Explicit%20Fields:%20The%20val%20Keyword%20\(F%23\).md).  
  
 You can also define private fields in a class by using a member definition and adding the keyword `private` to the definition. This can be useful if you expect to change the accessibility of a member without rewriting your code. For more information, see [Access Control](../vs140/Access-Control--F#-.md).  
  
## See Also  
 [Members (F#)](../vs140/Members--F#-.md)   
 [do Bindings in Classes](../vs140/do-Bindings-in-Classes--F#-.md)   
 [let Bindings](../vs140/let-Bindings--F#-.md)