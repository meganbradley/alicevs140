---
title: "Type Inference (F#)"
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
ms.assetid: 1064b523-4917-424c-9c4e-e4bf96ecae6f
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Type Inference (F#)
This topic describes how the F# compiler infers the types of values, variables, parameters and return values.  
  
## Type Inference in General  
 The idea of type inference is that you do not have to specify the types of F# constructs except when the compiler cannot conclusively deduce the type. Omitting explicit type information does not mean that F# is a dynamically typed language or that values in F# are weakly typed. F# is a statically typed language, which means that the compiler deduces an exact type for each construct during compilation. If there is not enough information for the compiler to deduce the types of each construct, you must supply additional type information, typically by adding explicit type annotations somewhere in the code.  
  
## Inference of Parameter and Return Types  
 In a parameter list, you do not have to specify the type of each parameter. And yet, F# is a statically typed language, and therefore every value and expression has a definite type at compile time. For those types that you do not specify explicitly, the compiler infers the type based on the context. If the type is not otherwise specified, it is inferred to be generic. If the code uses a value inconsistently, in such a way that there is no single inferred type that satisfies all the uses of a value, the compiler reports an error.  
  
 The return type of a function is determined by the type of the last expression in the function.  
  
 For example, in the following code, the parameter types `a` and `b` and the return type are all inferred to be `int` because the literal `100` is of type `int`.  
  
 [!CODE [FsLangRef3#301](../CodeSnippet/VS_Snippets_Fsharp/fslangref3#301)]  
  
 You can influence type inference by changing the literals. If you make the `100` a `uint32` by appending the suffix `u`, the types of `a`, `b`, and the return value are inferred to be `uint32`.  
  
 You can also influence type inference by using other constructs that imply restrictions on the type, such as functions and methods that work with only a particular type.  
  
 Also, you can apply explicit type annotations to function or method parameters or to variables in expressions, as shown in the following examples. Errors result if conflicts occur between different constraints.  
  
 [!CODE [FsLangRef3#302](../CodeSnippet/VS_Snippets_Fsharp/fslangref3#302)]  
  
 You can also explicitly specify the return value of a function by providing a type annotation after all the parameters.  
  
 [!CODE [FsLangRef3#303](../CodeSnippet/VS_Snippets_Fsharp/fslangref3#303)]  
  
 A common case where a type annotation is useful on a parameter is when the parameter is an object type and you want to use a member.  
  
 [!CODE [FsLangRef3#304](../CodeSnippet/VS_Snippets_Fsharp/fslangref3#304)]  
  
## Automatic Generalization  
 If the function code is not dependent on the type of a parameter, the compiler considers the parameter to be generic. This is called *automatic generalization*, and it can be a powerful aid to writing generic code without increasing complexity.  
  
 For example, the following function combines two parameters of any type into a tuple.  
  
 [!CODE [FsLangRef3#305](../CodeSnippet/VS_Snippets_Fsharp/fslangref3#305)]  
  
 The type is inferred to be  
  
```  
'a -> 'b -> 'a * 'b  
```  
  
## Additional Information  
 Type inference is described in more detail in the F# Language Specification.  
  
## See Also  
 [Automatic Generalization](../vs140/Automatic-Generalization--F#-.md)