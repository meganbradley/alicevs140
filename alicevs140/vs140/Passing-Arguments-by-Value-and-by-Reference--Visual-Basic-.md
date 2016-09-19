---
title: "Passing Arguments by Value and by Reference (Visual Basic)"
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
ms.assetid: fd8a9de6-7178-44d5-a9bf-458d4ad907c2
caps.latest.revision: 25
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Passing Arguments by Value and by Reference (Visual Basic)
In [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)], you can pass an argument to a procedure *by value* or *by reference*. This is known as the *passing mechanism*, and it determines whether the procedure can modify the programming element underlying the argument in the calling code. The procedure declaration determines the passing mechanism for each parameter by specifying the [ByVal](../vs140/ByVal--Visual-Basic-.md) or [ByRef](../vs140/ByRef--Visual-Basic-.md) keyword.  
  
## Distinctions  
 When passing an argument to a procedure, be aware of several different distinctions that interact with each other:  
  
-   Whether the underlying programming element is modifiable or nonmodifiable  
  
-   Whether the argument itself is modifiable or nonmodifiable  
  
-   Whether the argument is being passed by value or by reference  
  
-   Whether the argument data type is a value type or a reference type  
  
 For more information, see [Differences Between Modifiable and Nonmodifiable Arguments](../vs140/Differences-Between-Modifiable-and-Nonmodifiable-Arguments--Visual-Basic-.md) and [Differences Between Passing an Argument By Value and By Reference](../vs140/Differences-Between-Passing-an-Argument-By-Value-and-By-Reference--Visual-Basic-.md).  
  
## Choice of Passing Mechanism  
 You should choose the passing mechanism carefully for each argument.  
  
-   **Protection**. In choosing between the two passing mechanisms, the most important criterion is the exposure of calling variables to change. The advantage of passing an argument `ByRef` is that the procedure can return a value to the calling code through that argument. The advantage of passing an argument `ByVal` is that it protects a variable from being changed by the procedure.  
  
-   **Performance**. Although the passing mechanism can affect the performance of your code, the difference is usually insignificant. One exception to this is a value type passed `ByVal`. In this case, [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] copies the entire data contents of the argument. Therefore, for a large value type such as a structure, it can be more efficient to pass it `ByRef`.  
  
     For reference types, only the pointer to the data is copied (four bytes on 32-bit platforms, eight bytes on 64-bit platforms). Therefore, you can pass arguments of type `String` or `Object` by value without harming performance.  
  
## Determination of the Passing Mechanism  
 The procedure declaration specifies the passing mechanism for each parameter. The calling code can't override a `ByVal` mechanism.  
  
 If a parameter is declared with `ByRef`, the calling code can force the mechanism to `ByVal` by enclosing the argument name in parentheses in the call. For more information, see [How to: Force an Argument to Be Passed by Value (Visual Basic)](../vs140/How-to--Force-an-Argument-to-Be-Passed-by-Value--Visual-Basic-.md).  
  
 The default in [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] is to pass arguments by value.  
  
## When to Pass an Argument by Value  
  
-   If the calling code element underlying the argument is a nonmodifiable element, declare the corresponding parameter [ByVal](../vs140/ByVal--Visual-Basic-.md). No code can change the value of a nonmodifiable element.  
  
-   If the underlying element is modifiable, but you do not want the procedure to be able to change its value, declare the parameter `ByVal`. Only the calling code can change the value of a modifiable element passed by value.  
  
## When to Pass an Argument by Reference  
  
-   If the procedure has a genuine need to change the underlying element in the calling code, declare the corresponding parameter [ByRef](../vs140/ByRef--Visual-Basic-.md).  
  
-   If the correct execution of the code depends on the procedure changing the underlying element in the calling code, declare the parameter `ByRef`. If you pass it by value, or if the calling code overrides the `ByRef` passing mechanism by enclosing the argument in parentheses, the procedure call might produce unexpected results.  
  
## Example  
  
### Description  
 The following example illustrates when to pass arguments by value and when to pass them by reference. Procedure `Calculate` has both a `ByVal` and a `ByRef` parameter. Given an interest rate, `rate`, and a sum of money, `debt`, the task of the procedure is to calculate a new value for `debt` that is the result of applying the interest rate to the original value of `debt`. Because `debt` is a `ByRef` parameter, the new total is reflected in the value of the argument in the calling code that corresponds to `debt`. Parameter `rate` is a `ByVal` parameter because `Calculate` should not change its value.  
  
### Code  
 [!CODE [VbVbcnProcedures#74](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnProcedures#74)]  
  
## See Also  
 [Procedures in Visual Basic](../vs140/Procedures-in-Visual-Basic.md)   
 [Procedure Parameters and Arguments](../vs140/Procedure-Parameters-and-Arguments--Visual-Basic-.md)   
 [How to: Pass Arguments to a Procedure](../Topic/How%20to:%20Pass%20Arguments%20to%20a%20Procedure%20\(Visual%20Basic\).md)   
 [How to: Change the Value of a Procedure Argument](../vs140/How-to--Change-the-Value-of-a-Procedure-Argument--Visual-Basic-.md)   
 [How to: Protect a Procedure Argument Against Value Changes](../vs140/How-to--Protect-a-Procedure-Argument-Against-Value-Changes--Visual-Basic-.md)   
 [How to: Force an Argument to Be Passed by Value](../vs140/How-to--Force-an-Argument-to-Be-Passed-by-Value--Visual-Basic-.md)   
 [Argument Passing by Position and by Name](../vs140/Passing-Arguments-by-Position-and-by-Name--Visual-Basic-.md)   
 [Value Types and Reference Types](../Topic/Value%20Types%20and%20Reference%20Types.md)