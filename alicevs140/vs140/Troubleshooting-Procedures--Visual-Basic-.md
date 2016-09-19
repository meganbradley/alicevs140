---
title: "Troubleshooting Procedures (Visual Basic)"
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
ms.assetid: 525721e8-2e02-4f75-b5d8-6b893462cf2b
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Troubleshooting Procedures (Visual Basic)
This page lists some common problems that can occur when working with procedures.  
  
## Returning an Array Type from a Function Procedure  
 If a `Function` procedure returns an array data type, you cannot use the `Function` name to store values in the elements of the array. If you attempt to do this, the compiler interprets it as a call to the `Function`. The following example generates compiler errors.  
  
 `Function allOnes(ByVal n As Integer) As Integer()`  
  
 `For i As Integer = 1 To n - 1`  
  
 `' The following statement generates a`   `COMPILER ERROR`  `.`  
  
 `allOnes(i) = 1`  
  
 `Next i`  
  
 `' The following statement generates a`   `COMPILER ERROR`  `.`  
  
 `Return allOnes()`  
  
 `End Function`  
  
 The statement `allOnes(i) = 1` generates a compiler error because it appears to call `allOnes` with an argument of the wrong data type (a singleton `Integer` instead of an `Integer` array). The statement `Return allOnes()` generates a compiler error because it appears to call `allOnes` with no argument.  
  
 **Correct Approach:** To be able to modify the elements of an array that is to be returned, define an internal array as a local variable. The following example compiles without error.  
  
 [!CODE [VbVbcnProcedures#66](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnProcedures#66)]  
  
## Argument Not Being Modified by Procedure Call  
 If you intend to allow a procedure to change a programming element underlying an argument in the calling code, you must pass it by reference. But a procedure can access the elements of a reference type argument even if you pass it by value.  
  
-   **Underlying Variable**. To allow the procedure to replace the value of the underlying variable element itself, the procedure must declare the parameter [ByRef](../vs140/ByRef--Visual-Basic-.md). Also, the calling code must not enclose the argument in parentheses, because that would override the `ByRef` passing mechanism.  
  
-   **Reference Type Elements**. If you declare a parameter [ByVal](../vs140/ByVal--Visual-Basic-.md), the procedure cannot modify the underlying variable element itself. However, if the argument is a reference type, the procedure can modify the members of the object to which it points, even though it cannot replace the variable's value. For example, if the argument is an array variable, the procedure cannot assign a new array to it, but it can change one or more of its elements. The changed elements are reflected in the underlying array variable in the calling code.  
  
 The following example defines two procedures that take an array variable by value and operate on its elements. Procedure `increase` simply adds one to each element. Procedure `replace` assigns a new array to the parameter `a()` and then adds one to each element. However, the reassignment does not affect the underlying array variable in the calling code because `a()` is declared `ByVal`.  
  
 [!CODE [VbVbcnProcedures#35](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnProcedures#35)]  
  
 [!CODE [VbVbcnProcedures#38](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnProcedures#38)]  
  
 The following example makes calls to `increase` and `replace`.  
  
 [!CODE [VbVbcnProcedures#37](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnProcedures#37)]  
  
 The first `MsgBox` call displays "After increase(n): 11, 21, 31, 41". Because `n` is a reference type, `increase` can change its members, even though it is passed `ByVal`.  
  
 The second `MsgBox` call displays "After replace(n): 11, 21, 31, 41". Because `n` is passed `ByVal`, `replace` cannot modify the variable `n` by assigning a new array to it. When `replace` creates the new array instance `k` and assigns it to the local variable `a`, it loses the reference to `n` passed in by the calling code. When it increments the members of `a`, only the local array `k` is affected.  
  
 **Correct Approach:** To be able to modify an underlying variable element itself, pass it by reference. The following example shows the change in the declaration of `replace` that allows it to replace one array with another in the calling code.  
  
 [!CODE [VbVbcnProcedures#64](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnProcedures#64)]  
  
## Unable to Define an Overload  
 If you want to define an overloaded version of a procedure, you must use the same name but a different signature. If the compiler cannot differentiate your declaration from an overload with the same signature, it generates an error.  
  
 The *signature* of a procedure is determined by the procedure name and the parameter list. Each overload must have the same name as all the other overloads but must differ from all of them in at least one of the other components of the signature. For more information, see [Procedure Overloading](../Topic/Procedure%20Overloading%20\(Visual%20Basic\).md).  
  
 The following items, even though they pertain to the parameter list, are not components of a procedure's signature:  
  
-   Procedure modifier keywords, such as `Public`, `Shared`, and `Static`  
  
-   Parameter names  
  
-   Parameter modifier keywords, such as `ByRef` and `Optional`  
  
-   The data type of the return value (except for a conversion operator)  
  
 You cannot overload a procedure by varying only one or more of the preceding items.  
  
 **Correct Approach:** To be able to define a procedure overload, you must vary the signature. Because you must use the same name, you must vary the number, order, or data types of the parameters. In a generic procedure, you can vary the number of type parameters. In a conversion operator ([CType Function](../Topic/CType%20Function%20\(Visual%20Basic\).md)), you can vary the return type.  
  
### Overload Resolution with Optional and ParamArray Arguments  
 If you are overloading a procedure with one or more [Optional (Visual Basic)](../vs140/Optional--Visual-Basic-.md) parameters or a [ParamArray](../vs140/ParamArray--Visual-Basic-.md) parameter, you must avoid duplicating any of the *implicit overloads*. For information, see [Considerations in Overloading Procedures](../vs140/Considerations-in-Overloading-Procedures--Visual-Basic-.md).  
  
## Calling a Wrong Version of an Overloaded Procedure  
 If a procedure has several overloaded versions, you should be familiar with all their parameter lists and understand how [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] resolves calls among the overloads. Otherwise you could call an overload other than the intended one.  
  
 When you have determined which overload you want to call, be careful to observe the following rules:  
  
-   Supply the correct number of arguments, and in the correct order.  
  
-   Ideally, your arguments should have the exact same data types as the corresponding parameters. In any case, the data type of each argument must widen to that of its corresponding parameter. This is true even with the [Option Strict Statement](../vs140/Option-Strict-Statement.md) set to `Off`. If an overload requires any narrowing conversion from your argument list, that overload is not eligible to be called.  
  
-   If you supply arguments that require widening, make their data types as close as possible to the corresponding parameter data types. If two or more overloads accept your argument data types, the compiler resolves your call to the overload that calls for the least amount of widening.  
  
 You can reduce the chance of data type mismatches by using the [CType Function](../Topic/CType%20Function%20\(Visual%20Basic\).md) conversion keyword when preparing your arguments.  
  
### Overload Resolution Failure  
 When you call an overloaded procedure, the compiler attempts to eliminate all but one of the overloads. If it succeeds, it resolves the call to that overload. If it eliminates all the overloads, or if it cannot reduce the eligible overloads to a single candidate, it generates an error.  
  
 The following example illustrates the overload resolution process.  
  
 [!CODE [VbVbcnProcedures#62](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnProcedures#62)]  
  
 [!CODE [VbVbcnProcedures#63](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnProcedures#63)]  
  
 In the first call, the compiler eliminates the first overload because the type of the first argument (`Short`) narrows to the type of the corresponding parameter (`Byte`). It then eliminates the third overload because each argument type in the second overload (`Short` and `Single`) widens to the corresponding type in the third overload (`Integer` and `Single`). The second overload requires less widening, so the compiler uses it for the call.  
  
 In the second call, the compiler cannot eliminate any of the overloads on the basis of narrowing. It eliminates the third overload for the same reason as in the first call, because it can call the second overload with less widening of the argument types. However, the compiler cannot resolve between the first and second overloads. Each has one defined parameter type that widens to the corresponding type in the other (`Byte` to `Short`, but `Single` to `Double`). The compiler therefore generates an overload resolution error.  
  
 **Correct Approach:** To be able to call an overloaded procedure without ambiguity, use [CType Function](../Topic/CType%20Function%20\(Visual%20Basic\).md) to match the argument data types to the parameter types. The following example shows a call to `z` that forces resolution to the second overload.  
  
 [!CODE [VbVbcnProcedures#65](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnProcedures#65)]  
  
### Overload Resolution with Optional and ParamArray Arguments  
 If two overloads of a procedure have identical signatures except that the last parameter is declared [Optional (Visual Basic)](../vs140/Optional--Visual-Basic-.md) in one and [ParamArray](../vs140/ParamArray--Visual-Basic-.md) in the other, the compiler resolves a call to that procedure according to the closest match. For more information, see [Overload Resolution](../vs140/Overload-Resolution--Visual-Basic-.md).  
  
## See Also  
 [Procedures in Visual Basic](../vs140/Procedures-in-Visual-Basic.md)   
 [Sub Procedures](../vs140/Sub-Procedures--Visual-Basic-.md)   
 [Function Procedures](../Topic/Function%20Procedures%20\(Visual%20Basic\).md)   
 [Property Procedures](../vs140/Property-Procedures--Visual-Basic-.md)   
 [Operator Procedures](../vs140/Operator-Procedures--Visual-Basic-.md)   
 [Procedure Parameters and Arguments](../vs140/Procedure-Parameters-and-Arguments--Visual-Basic-.md)   
 [Procedure Overloading](../Topic/Procedure%20Overloading%20\(Visual%20Basic\).md)   
 [Considerations in Overloading Procedures](../vs140/Considerations-in-Overloading-Procedures--Visual-Basic-.md)   
 [Overload Resolution](../vs140/Overload-Resolution--Visual-Basic-.md)