---
title: "Flexible Types (F#)"
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
ms.assetid: 4ce3f8b6-b852-4c38-b78f-3c1988ce982a
caps.latest.revision: 25
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Flexible Types (F#)
A *flexible type annotation* indicates that a parameter, variable, or value has a type that is compatible with a specifed type, where compatibility is determined by position in an object-oriented hierarchy of classes or interfaces. Flexible types are useful specifically when the automatic conversion to types higher in the type hierarchy does not occur but you still want to enable your functionality to work with any type in the hierarchy or any type that implements an interface.  
  
## Syntax  
  
```  
#type  
```  
  
## Remarks  
 In the previous syntax, `type` represents a base type or an interface.  
  
 A flexible type is equivalent to a generic type that has a constraint that limits the allowed types to types that are compatible with the base or interface type. That is, the following two lines of code are equivalent.  
  
 `#SomeType`  
  
 `'a when 'a :> SomeType`  
  
 Flexible types are useful in several types of situations. For example, when you have a higher order function (a function that takes a function as an argument), it is often useful to have the function return a flexible type. In the following example, the use of a flexible type with a sequence argument in `iterate2` enables the higher order function to work with functions that generate sequences, arrays, lists, and any other enumerable type.  
  
 Consider the following two functions, one of which returns a sequence, the other of which returns a flexible type.  
  
 [!CODE [FsLangRef2#4101](../CodeSnippet/VS_Snippets_Fsharp/fslangref2#4101)]  
  
 As another example, consider the [Seq.concat](../Topic/Seq.concat%3C'Collection,'T%3E%20Function%20\(F%23\).md) library function:  
  
```  
val concat: sequences:seq<#seq<'T>> -> seq<'T>  
```  
  
 You can pass any of the following enumerable sequences to this function:  
  
-   A list of lists  
  
-   A list of arrays  
  
-   An array of lists  
  
-   An array of sequences  
  
-   Any other combination of enumerable sequences  
  
 The following code uses `Seq.concat` to demonstrate the scenarios that you can support by using flexible types.  
  
 [!CODE [FsLangRef2#4102](../CodeSnippet/VS_Snippets_Fsharp/fslangref2#4102)]  
  
 The output is as follows.  
  
```  
seq [1; 2; 3; 4; ...]  
seq [1; 2; 3; 4; ...]  
seq [1; 2; 3; 4; ...]  
seq [1; 2; 3; 4; ...]  
seq [1; 2; 3; 4; ...]  
```  
  
 In F#, as in other object-oriented languages, there are contexts in which derived types or types that implement interfaces are automatically converted to a base type or interface type. These automatic conversions occur in direct arguments, but not when the type is in a subordinate position, as part of a more complex type such as a return type of a function type, or as a type argument. Thus, the flexible type notation is primarily useful when the type you are applying it to is part of a more complex type.  
  
## See Also  
 [F# Language Reference](../Topic/F%23%20Language%20Reference.md)   
 [Generics (F#)](../vs140/Generics--F#-.md)