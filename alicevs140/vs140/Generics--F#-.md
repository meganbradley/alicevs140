---
title: "Generics (F#)"
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
ms.assetid: 724af101-7b0d-4c0c-a0c1-25b8005f8e27
caps.latest.revision: 32
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Generics (F#)
F# function values, methods, properties, and aggregate types such as classes, records, and discriminated unions can be *generic*. Generic constructs contain at least one type parameter, which is usually supplied by the user of the generic construct. Generic functions and types enable you to write code that works with a variety of types without repeating the code for each type. Making your code generic can be simple in F#, because often your code is implicitly inferred to be generic by the compiler's type inference and automatic generalization mechanisms.  
  
## Syntax  
  
```  
// Explicitly generic function.  
let function-name<type-parameters> parameter-list =  
   function-body  
  
// Explicitly generic method.  
[ static ] member object-identifer.method-name<type-parameters> parameter-list [ return-type ] =  
   method-body  
  
// Explicitly generic class, record, interface, structure,  
// or discriminated union.  
type type-name<type-parameters> type-definition  
```  
  
## Remarks  
 The declaration of an explicitly generic function or type is much like that of a non-generic function or type, except for the specification (and use) of the type parameters, in angle brackets after the function or type name.  
  
 Declarations are often implicitly generic. If you do not fully specify the type of every parameter that is used to compose a function or type, the compiler attempts to infer the type of each parameter, value, and variable from the code you write. For more information, see [Type Inference](../vs140/Type-Inference--F#-.md). If the code for your type or function does not otherwise constrain the types of parameters, the function or type is implicitly generic. This process is named *automatic generalization*. There are some limits on automatic generalization. For example, if the F# compiler is unable to infer the types for a generic construct, the compiler reports an error that refers to a restriction called the *value restriction*. In that case, you may have to add some type annotations. For more information about automatic generalization and the value restriction, and how to change your code to address the problem, see [Automatic Generalization (F#)](../vs140/Automatic-Generalization--F#-.md).  
  
 In the previous syntax, `type-parameters` is a comma-separated list of parameters that represent unknown types, each of which starts with a single quotation mark, optionally with a constraint clause that further limits what types may be used for that type parameter. For the syntax for constraint clauses of various kinds and other information about constraints, see [Constraints (F#)](../vs140/Constraints--F#-.md).  
  
 The `type-definition` in the syntax is the same as the type definition for a non-generic type. It includes the constructor parameters for a class type, an optional `as` clause, the equal symbol, the record fields, the `inherit` clause, the choices for a discriminated union, `let` and `do` bindings, member definitions, and anything else permitted in a non-generic type definition.  
  
 The other syntax elements are the same as those for non-generic functions and types. For example, `object-identifier` is an identifier that represents the containing object itself.  
  
 Properties, fields, and constructors cannot be more generic than the enclosing type. Also, values in a module cannot be generic.  
  
## Implicitly Generic Constructs  
 When the F# compiler infers the types in your code, it automatically treats any function that can be generic as generic. If you specify a type explicitly, such as a parameter type, you prevent automatic generalization.  
  
 In the following code example, `makeList` is generic, even though neither it nor its parameters are explicitly declared as generic.  
  
 [!CODE [FsLangRef1#1700](../CodeSnippet/VS_Snippets_Fsharp/fslangref1#1700)]  
  
 The signature of the function is inferred to be `'a -> 'a -> 'a list`. Note that `a` and `b` in this example are inferred to have the same type. This is because they are included in a list together, and all elements of a list must be of the same type.  
  
 You can also make a function generic by using the single quotation mark syntax in a type annotation to indicate that a parameter type is a generic type parameter. In the following code, `function1` is generic because its parameters are declared in this manner, as type parameters.  
  
 [!CODE [FsLangRef1#1701](../CodeSnippet/VS_Snippets_Fsharp/fslangref1#1701)]  
  
## Explicitly Generic Constructs  
 You can also make a function generic by explicitly declaring its type parameters in angle brackets (< >). The following code illustrates this.  
  
 [!CODE [FsLangRef1#1703](../CodeSnippet/VS_Snippets_Fsharp/fslangref1#1703)]  
  
## Using Generic Constructs  
 When you use generic functions or methods, you might not have to specify the type arguments. The compiler uses type inference to infer the appropriate type arguments. If there is still an ambiguity, you can supply type arguments in angle brackets, separating multiple type arguments with commas.  
  
 The following code shows the use of the functions that are defined in the previous sections.  
  
 [!CODE [FsLangRef1#1702](../CodeSnippet/VS_Snippets_Fsharp/fslangref1#1702)]  
  
> [!NOTE]
>  There are two ways to refer to a generic type by name. For example, `list<int>` and `int list` are two ways to refer to a generic type `list` that has a single type argument `int`. The latter form is conventionally used only with built-in F# types such as `list` and `option`. If there are multiple type arguments, you normally use the syntax `Dictionary<int, string>` but you can also use the syntax `(int, string) Dictionary`.  
  
## Wildcards as Type Arguments  
 To specify that a type argument should be inferred by the compiler, you can use the underscore, or wildcard symbol (_), instead of a named type argument. This is shown in the following code.  
  
 [!CODE [FsLangRef1#1704](../CodeSnippet/VS_Snippets_Fsharp/fslangref1#1704)]  
  
## Constraints in Generic Types and Functions  
 In a generic type or function definition, you can use only those constructs that are known to be available on the generic type parameter. This is required to enable the verification of function and method calls at compile time. If you declare your type parameters explicitly, you can apply an explicit constraint to a generic type parameter to notify the compiler that certain methods and functions are available. However, if you allow the F# compiler to infer your generic parameter types, it will determine the appropriate constraints for you. For more information, see [Constraints (F#)](../vs140/Constraints--F#-.md).  
  
## Statically Resolved Type Parameters  
 There are two kinds of type parameters that can be used in F# programs. The first are generic type parameters of the kind described in the previous sections. This first kind of type parameter is equivalent to the generic type parameters that are used in languages such as Visual Basic and C#. Another kind of type parameter is specific to F# and is referred to as a *statically resolved type parameter*. For information about these constructs, see [Statically Resolved Type Parameters](../vs140/Statically-Resolved-Type-Parameters--F#-.md).  
  
## Examples  
 [!CODE [FsLangRef1#1705](../CodeSnippet/VS_Snippets_Fsharp/fslangref1#1705)]  
  
## See Also  
 [F# Language Reference](../Topic/F%23%20Language%20Reference.md)   
 [F# Types](../vs140/F#-Types.md)   
 [Statically Resolved Type Parameters](../vs140/Statically-Resolved-Type-Parameters--F#-.md)   
 [Generics in the .NET Framework](assetId:///2994d786-c5c7-4666-ab23-4c83129fe39c)   
 [Automatic Generalization](../vs140/Automatic-Generalization--F#-.md)   
 [Constraints](../vs140/Constraints--F#-.md)