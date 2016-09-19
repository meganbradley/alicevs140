---
title: "Local Type Inference (Visual Basic)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-visual-basic
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b8307f18-2e56-4ab3-a45a-826873f400f6
caps.latest.revision: 45
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Local Type Inference (Visual Basic)
The Visual Basic compiler uses *type inference* to determine the data types of local variables declared without an `As` clause. The compiler infers the type of the variable from the type of the initialization expression. This enables you to declare variables without explicitly stating a type, as shown in the following example. As a result of the declarations, both `num1` and `num2` are strongly typed as integers.  
  
 [!CODE [VbVbalrTypeInference#1](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrTypeInference#1)]  
  
> [!NOTE]
>  If you do not want `num2` in the previous example to be typed as an `Integer`, you can specify another type by using a declaration like `Dim num3 As Object = 3` or `Dim num4 As Double = 3`.  
  
 Local type inference applies at procedure level. It cannot be used to declare variables at module level (within a class, structure, module, or interface but not within a procedure or block). If `num2` in the previous example were a field of a class instead of a local variable in a procedure, the declaration would cause an error with `Option Strict` on, and would classify `num2` as an `Object` with `Option Strict` off. Similarly, local type inference does not apply to procedure level variables declared as `Static`.  
  
## Type Inference vs. Late Binding  
 Code that uses type inference resembles code that relies on late binding. However, type inference strongly types the variable instead of leaving it as `Object`. The compiler uses a variable's initializer to determine the variable's type at compile time to produce early-bound code. In the previous example, `num2`, like `num1`, is typed as an `Integer`.  
  
 The behavior of early-bound variables differs from that of late-bound variables, for which the type is known only at run time. Knowing the type early enables the compiler to identify problems before execution, allocate memory precisely, and perform other optimizations. Early binding also enables the Visual Basic integrated development environment (IDE) to provide IntelliSense Help about the members of an object. Early binding is also preferred for performance. This is because all data stored in a late-bound variable must be wrapped as type `Object`, and accessing members of the type at run time makes the program slower.  
  
## Examples  
 Type inference occurs when a local variable is declared without an `As` clause and initialized. The compiler uses the type of the assigned initial value as the type of the variable. For example, each of the following lines of code declares a variable of type `String`.  
  
 [!CODE [VbVbalrTypeInference#2](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrTypeInference#2)]  
  
 The following code demonstrates two equivalent ways to create an array of integers.  
  
 [!CODE [VbVbalrTypeInference#3](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrTypeInference#3)]  
  
 It is convenient to use type inference to determine the type of a loop control variable. In the following code, the compiler infers that `number` is an `Integer` because `someNumbers2` from the previous example is an array of integers.  
  
 [!CODE [VbVbalrTypeInference#4](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrTypeInference#4)]  
  
 Local type inference can be used in `Using` statements to establish the type of the resource name, as the following example demonstrates.  
  
 [!CODE [VbVbalrTypeInference#7](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrTypeInference#7)]  
  
 The type of a variable can also be inferred from the return values of functions, as the following example demonstrates. Both `pList1` and `pList2` are arrays of processes because `Process.GetProcesses` returns an array of processes.  
  
 [!CODE [VbVbalrTypeInference#5](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrTypeInference#5)]  
  
## Option Infer  
 `Option Infer` enables you specify whether local type inference is allowed in a particular file. To enable or to block the option, type one of the following statements at the start of the file.  
  
 `Option Infer On`  
  
 `Option Infer Off`  
  
 If you do not specify a value for `Option Infer` in your code, the compiler default is `Option Infer On`. For projects upgraded from [!INCLUDE[vb_orcas_long](../vs140/includes/vb_orcas_long_md.md)] or earlier, the compiler default is `Option Infer Off`.  
  
 If the value set for `Option Infer` in a file conflicts with the value set in the IDE or on the command line, the value in the file has precedence.  
  
 For more information, see [Option Infer Statement](../vs140/Option-Infer-Statement.md) and [Compile Page, Project Designer (Visual Basic)](../vs140/Compile-Page--Project-Designer--Visual-Basic-.md).  
  
## Restrictions  
 Type inference can be used only for non-static local variables; it cannot be used to determine the type of class fields, properties, or functions.  
  
## See Also  
 [Anonymous Types](../Topic/Anonymous%20Types%20\(Visual%20Basic\).md)   
 [Early and Late Binding](../vs140/Early-and-Late-Binding--Visual-Basic-.md)   
 [For Each...Next Statement (Visual Basic)](../Topic/For%20Each...Next%20Statement%20\(Visual%20Basic\).md)   
 [For...Next Statement (Visual Basic)](../Topic/For...Next%20Statement%20\(Visual%20Basic\).md)   
 [Option Infer Statement](../vs140/Option-Infer-Statement.md)   
 [/optioninfer](../vs140/-optioninfer.md)   
 [Introduction to LINQ in Visual Basic](../Topic/Introduction%20to%20LINQ%20in%20Visual%20Basic.md)