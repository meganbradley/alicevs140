---
title: "How to: Protect a Procedure Argument Against Value Changes (Visual Basic)"
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
ms.assetid: d2b7c766-ce16-4d2c-8d79-3fc0e7ba2227
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Protect a Procedure Argument Against Value Changes (Visual Basic)
If a procedure declares a parameter as [ByRef](../vs140/ByRef--Visual-Basic-.md), [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] gives the procedure code a direct reference to the programming element underlying the argument in the calling code. This permits the procedure to change the value underlying the argument in the calling code. In some cases the calling code might want to protect against such a change.  
  
 You can always protect an argument from change by declaring the corresponding parameter [ByVal](../vs140/ByVal--Visual-Basic-.md) in the procedure. If you want to be able to change a given argument in some cases but not others, you can declare it `ByRef` and let the calling code determine the passing mechanism in each call. It does this by enclosing the corresponding argument in parentheses to pass it by value, or not enclosing it in parentheses to pass it by reference. For more information, see [How to: Force an Argument to Be Passed by Value](../vs140/How-to--Force-an-Argument-to-Be-Passed-by-Value--Visual-Basic-.md).  
  
## Example  
 The following example shows two procedures that take an array variable and operate on its elements. The `increase` procedure simply adds one to each element. The `replace` procedure assigns a new array to the parameter `a()` and then adds one to each element. However, the reassignment does not affect the underlying array variable in the calling code.  
  
 [!CODE [VbVbcnProcedures#35](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnProcedures#35)]  
  
 [!CODE [VbVbcnProcedures#38](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnProcedures#38)]  
  
 [!CODE [VbVbcnProcedures#37](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnProcedures#37)]  
  
 The first `MsgBox` call displays "After increase(n): 11, 21, 31, 41". Because the array `n` is a reference type, `replace` can change its members, even though the passing mechanism is `ByVal`.  
  
 The second `MsgBox` call displays "After replace(n): 11, 21, 31, 41". Because `n` is passed `ByVal`, `replace` cannot modify the variable `n` in the calling code by assigning a new array to it. When `replace` creates the new array instance `k` and assigns it to the local variable `a`, it loses the reference to `n` passed in by the calling code. When it changes the members of `a`, only the local array `k` is affected. Therefore, `replace` does not increment the values of array `n` in the calling code.  
  
## Compiling the Code  
 The default in [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] is to pass arguments by value. However, it is good programming practice to include either the [ByVal](../vs140/ByVal--Visual-Basic-.md) or [ByRef](../vs140/ByRef--Visual-Basic-.md) keyword with every declared parameter. This makes your code easier to read.  
  
## See Also  
 [Procedures in Visual Basic](../vs140/Procedures-in-Visual-Basic.md)   
 [Procedure Parameters and Arguments](../vs140/Procedure-Parameters-and-Arguments--Visual-Basic-.md)   
 [How to: Pass Arguments to a Procedure](../Topic/How%20to:%20Pass%20Arguments%20to%20a%20Procedure%20\(Visual%20Basic\).md)   
 [Argument Passing By Value and By Reference](../vs140/Passing-Arguments-by-Value-and-by-Reference--Visual-Basic-.md)   
 [Differences Between Variable and Nonvariable Arguments](../vs140/Differences-Between-Modifiable-and-Nonmodifiable-Arguments--Visual-Basic-.md)   
 [Differences Between Passing an Argument By Value and By Reference](../vs140/Differences-Between-Passing-an-Argument-By-Value-and-By-Reference--Visual-Basic-.md)   
 [How to: Change the Value of a Procedure Argument](../vs140/How-to--Change-the-Value-of-a-Procedure-Argument--Visual-Basic-.md)   
 [How to: Force an Argument to Be Passed by Value](../vs140/How-to--Force-an-Argument-to-Be-Passed-by-Value--Visual-Basic-.md)   
 [Argument Passing by Position and by Name](../vs140/Passing-Arguments-by-Position-and-by-Name--Visual-Basic-.md)   
 [Value Types and Reference Types](../Topic/Value%20Types%20and%20Reference%20Types.md)