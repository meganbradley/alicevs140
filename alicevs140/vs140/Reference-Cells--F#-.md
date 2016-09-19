---
title: "Reference Cells (F#)"
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
ms.assetid: 1e51a4aa-6c4b-47f5-90a3-ca005eebc41c
caps.latest.revision: 24
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Reference Cells (F#)
*Reference cells* are storage locations that enable you to create mutable values with reference semantics.  
  
## Syntax  
  
```  
ref expression  
```  
  
## Remarks  
 You use the `ref` operator before a value to create a new reference cell that encapsulates the value. You can then change the underlying value because it is mutable.  
  
 A reference cell holds an actual value; it is not just an address. When you create a reference cell by using the `ref` operator, you create a copy of the underlying value as an encapsulated mutable value.  
  
 You can dereference a reference cell by using the `!` (bang) operator.  
  
 The following code example illustrates the declaration and use of reference cells.  
  
 [!CODE [FsLangRef1#2201](../CodeSnippet/VS_Snippets_Fsharp/fslangref1#2201)]  
  
 The output is `50`.  
  
 Reference cells are instances of the `Ref` generic record type, which is declared as follows.  
  
```f#  
type Ref<'a> =  
    { mutable contents: 'a }  
```  
  
 The type `'a ref` is a synonym for `Ref<'a>`. The compiler and IntelliSense in the IDE display the former for this type, but the underlying definition is the latter.  
  
 The `ref` operator creates a new reference cell. The following code is the declaration of the `ref` operator.  
  
```f#  
let ref x = { contents = x }  
```  
  
 The following table shows the features that are available on the reference cell.  
  
|Operator, member, or field|Description|Type|Definition|  
|--------------------------------|-----------------|----------|----------------|  
|`!` (dereference operator)|Returns the underlying value.|`'a ref -> 'a`|`let (!) r = r.contents`|  
|`:=` (assignment operator)|Changes the underlying value.|`'a ref -> 'a -> unit`|`let (:=) r x = r.contents <- x`|  
|`ref` (operator)|Encapsulates a value into a new reference cell.|`'a -> 'a ref`|`let ref x = { contents = x }`|  
|`Value` (property)|Gets or sets the underlying value.|`unit -> 'a`|`member x.Value = x.contents`|  
|`contents` (record field)|Gets or sets the underlying value.|`'a`|`let ref x = { contents = x }`|  
  
 There are several ways to access the underlying value. The value returned by the dereference operator (`!`) is not an assignable value. Therefore, if you are modifying the underlying value, you must use the assignment operator (`:=`) instead.  
  
 Both the `Value` property and the `contents` field are assignable values. Therefore, you can use these to either access or change the underlying value, as shown in the following code.  
  
 [!CODE [FsLangRef1#2203](../CodeSnippet/VS_Snippets_Fsharp/fslangref1#2203)]  
  
 The output is as follows.  
  
```  
10  
10  
11  
12  
```  
  
 The field `contents` is provided for compatibility with other versions of ML and will produce a warning during compilation. To disable the warning, use the `--mlcompatibility` compiler option. For more information, see [Compiler Options](../vs140/Compiler-Options--F#-.md).  
  
## Example  
 The following code illustrates the use of reference cells in parameter passing. The `Incrementor` type has a method `Increment` that takes a parameter that includes `byref` in the parameter type. The `byref` in the parameter type indicates that callers must pass a reference cell or the address of a typical variable of the specified type, in this case `int`. The remaining code illustrates how to call `Increment` with both of these types of arguments, and shows the use of the `ref` operator on a variable to create a reference cell (`ref myDelta1`). It then shows the use of the address-of operator (`&`) to generate an appropriate argument. Finally, the `Increment` method is called again by using a reference cell that is declared by using a `let` binding. The final line of code demonstrates the use of the `!` operator to dereference the reference cell for printing.  
  
 [!CODE [FsLangRef1#2204](../CodeSnippet/VS_Snippets_Fsharp/fslangref1#2204)]  
  
 For more information about how to pass by reference, see [Passing Arguments (F#)](../Topic/Parameters%20and%20Arguments%20\(F%23\).md).  
  
> [!NOTE]
>  C# programmers should know that `ref` works differently in F# than it does in C#. For example, the use of `ref` when you pass an argument does not have the same effect in F# as it does in C#.  
  
## Reference Cells vs. Mutable Variables  
 Reference cells and mutable variables can often be used in the same situations. However, there are some situations in which mutable variables cannot be used, and you must use a reference cell instead. In general, you should prefer mutable variables where they are accepted by the compiler. However, in expressions that generate closures, the compiler will report that you cannot use mutable variables. *Closures* are local functions that are generated by certain F# expressions, such as lambda expressions, sequence expressions, computation expressions, and curried functions that use partially applied arguments. The closures generated by these expressions are stored for later evaluation. This process is not compatible with mutable variables. Therefore, if you need mutable state in such an expression, you have to use reference cells. For more information about closures, see Closures (F#).  
  
 The following code example demonstrates the scenario in which you must use a reference cell.  
  
 [!CODE [FsLangRef1#2205](../CodeSnippet/VS_Snippets_Fsharp/fslangref1#2205)]  
  
 In the previous code, the reference cell `finished` is included in local state, that is, variables that are in the closure are created and used entirely within the expression, in this case a sequence expression. Consider what occurs when the variables are non-local. Closures can also access non-local state, but when this occurs, the variables are copied and stored by value. This process is known as *value semantics*. This means that the values at the time of the copy are stored, and any subsequent changes to the variables are not reflected. If you want to track the changes of non-local variables, or, in other words, if you need a closure that interacts with non-local state by using *reference semantics*, you must use a reference cell.  
  
 The following code examples demonstrate the use of reference cells in closures. In this case, the closure results from the partial application of function arguments.  
  
 [!CODE [FsLangRef1#2207](../CodeSnippet/VS_Snippets_Fsharp/fslangref1#2207)]  
  
## See Also  
 [F# Language Reference](../Topic/F%23%20Language%20Reference.md)   
 [Passing Arguments](../Topic/Parameters%20and%20Arguments%20\(F%23\).md)   
 [Symbol and Operator Reference](../vs140/Symbol-and-Operator-Reference--F#-.md)