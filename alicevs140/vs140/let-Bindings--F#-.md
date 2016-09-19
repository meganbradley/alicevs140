---
title: "let Bindings (F#)"
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
ms.assetid: c3b2cc64-04e1-4366-bfba-e8c71b96d86c
caps.latest.revision: 34
translation.priority.ht: 
  - de-de
  - ja-jp
---
# let Bindings (F#)
A *binding* associates an identifier with a value or function. You use the `let` keyword to bind a name to a value or function.  
  
## Syntax  
  
```  
// Binding a value:  
let identifier-or-pattern [: type] =  
   expression  
body-expression  
// Binding a function value:  
let identifier parameter-list [: return-type ] =  
   expression  
body-expression  
```  
  
## Remarks  
 The `let` keyword is used in binding expressions to define values or function values for one or more names. The simplest form of the `let` expression binds a name to a simple value, as follows.  
  
 [!CODE [FsLangRef1#1101](../CodeSnippet/VS_Snippets_Fsharp/fslangref1#1101)]  
  
 If you separate the expression from the identifier by using a new line, you must indent each line of the expression, as in the following code.  
  
 [!CODE [FsLangRef1#1102](../CodeSnippet/VS_Snippets_Fsharp/fslangref1#1102)]  
  
 Instead of just a name, a pattern that contains names can be specified, for example, a tuple, as shown in the following code.  
  
 [!CODE [FsLangRef1#1103](../CodeSnippet/VS_Snippets_Fsharp/fslangref1#1103)]  
  
 The `body-expression` is the expression in which the names are used. The body expression appears on its own line, indented to line up exactly with the first character in the `let` keyword:  
  
 [!CODE [FsLangRef1#1104](../CodeSnippet/VS_Snippets_Fsharp/fslangref1#1104)]  
  
 A `let` binding can appear at the module level, in the definition of a class type, or in local scopes, such as in a function definition. A `let` binding at the top level in a module or in a class type does not need to have a body expression, but at other scope levels, the body expression is required. The bound names are usable after the point of definition, but not at any point before the `let` binding appears, as is illustrated in the following code.  
  
 [!CODE [FsLangRef1#1105](../CodeSnippet/VS_Snippets_Fsharp/fslangref1#1105)]  
  
## Function Bindings  
 Function bindings follow the rules for value bindings, except that function bindings include the function name and the parameters, as shown in the following code.  
  
 [!CODE [FsLangRef1#1106](../CodeSnippet/VS_Snippets_Fsharp/fslangref1#1106)]  
  
 In general, parameters are patterns, such as a tuple pattern:  
  
 [!CODE [FsLangRef1#1107](../CodeSnippet/VS_Snippets_Fsharp/fslangref1#1107)]  
  
 A `let` binding expression evaluates to the value of the last expression. Therefore, in the following code example, the value of `result` is computed from `100 * function3 (1, 2)`, which evaluates to `300`.  
  
 [!CODE [FsLangRef1#1109](../CodeSnippet/VS_Snippets_Fsharp/fslangref1#1109)]  
  
 For more information, see [Functions (F#)](../vs140/Functions--F#-.md).  
  
## Type Annotations  
 You can specify types for parameters by including a colon (:) followed by a type name, all enclosed in parentheses. You can also specify the type of the return value by appending the colon and type after the last parameter. The full type annotations for `function1`, with integers as the parameter types, would be as follows.  
  
 [!CODE [FsLangRef1#1108](../CodeSnippet/VS_Snippets_Fsharp/fslangref1#1108)]  
  
 When there are no explicit type parameters, type inference is used to determine the types of parameters of functions. This can include automatically generalizing the type of a parameter to be generic.  
  
 For more information, see [Automatic Generalization](../vs140/Automatic-Generalization--F#-.md) and [Type Inference](../vs140/Type-Inference--F#-.md).  
  
## let Bindings in Classes  
 A `let` binding can appear in a class type but not in a structure or record type. To use a let binding in a class type, the class must have a primary constructor. Constructor parameters must appear after the type name in the class definition. A `let` binding in a class type defines private fields and members for that class type and, together with `do` bindings in the type, forms the code for the primary constructor for the type. The following code examples show a class `MyClass` with private fields `field1` and `field2`.  
  
 [!CODE [FsLangRef1#1110](../CodeSnippet/VS_Snippets_Fsharp/fslangref1#1110)]  
  
 The scopes of `field1` and `field2` are limited to the type in which they are declared. For more information, see [Let Bindings in Classes](../vs140/let-Bindings-in-Classes--F#-.md) and [Classes (F#)](../vs140/Classes--F#-.md).  
  
## Type Parameters in let Bindings  
 A `let` binding at the module level, in a type, or in a computation expression can have explicit type parameters. A let binding in an expression, such as within a function definition, cannot have type parameters. For more information, see [Generics](../vs140/Generics--F#-.md).  
  
## Attributes on let Bindings  
 Attributes can be applied to top-level `let` bindings in a module, as shown in the following code.  
  
 [!CODE [FsLangRef1#1111](../CodeSnippet/VS_Snippets_Fsharp/fslangref1#1111)]  
  
## Scope and Accessibility of Let Bindings  
 The scope of an entity declared with a let binding is limited to the portion of the containing scope (such as a function, module, file or class) after the binding appears. Therefore, it can be said that a let binding introduces a name into a scope. In a module, a let-bound value or function is accessible to clients of a module as long as the module is accessible, since the let bindings in a module are compiled into public functions of the module. By contrast, let bindings in a class are private to the class.  
  
 Normally, functions in modules must be qualified by the name of the module when used by client code. For example, if a module `Module1` has a function `function1`, users would specify `Module1.function1` to refer to the function.  
  
 Users of a module may use an import declaration to make the functions within that module available for use without being qualified by the module name. In the example just mentioned, users of the module can in that case open the module by using the import declaration open `Module1` and thereafter refer to `function1` directly.  
  
```  
module Module1 =  
    let function1 x = x + 1.0  
  
module Module2 =  
    let function2 x =  
        Module1.function1 x  
  
    open Module1  
    let function3 x =  
        function1 x  
```  
  
 Some modules have the attribute [RequireQualifiedAccess](../vs140/Core.RequireQualifiedAccessAttribute-Class--F#-.md), which means that the functions that they expose must be qualified with the name of the module. For example, the F# List module has this attribute.  
  
 For more information on modules and access control, see [Modules (F#)](../vs140/Modules--F#-.md) and [Access Control (F#)](../vs140/Access-Control--F#-.md).  
  
## See Also  
 [Functions (F#)](../vs140/Functions--F#-.md)   
 [let Bindings in Classes (F#)](../vs140/let-Bindings-in-Classes--F#-.md)