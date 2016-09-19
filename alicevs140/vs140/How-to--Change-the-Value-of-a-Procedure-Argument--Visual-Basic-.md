---
title: "How to: Change the Value of a Procedure Argument (Visual Basic)"
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
ms.assetid: 6fad2368-5da7-4c07-8bf8-0f4e65a1be67
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Change the Value of a Procedure Argument (Visual Basic)
When you call a procedure, each argument you supply corresponds to one of the parameters defined in the procedure. In some cases, the procedure code can change the value underlying an argument in the calling code. In other cases, the procedure can change only its local copy of an argument.  
  
 When you call the procedure, [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] makes a local copy of every argument that is passed [ByVal](../vs140/ByVal--Visual-Basic-.md). For each argument passed [ByRef](../vs140/ByRef--Visual-Basic-.md), [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] gives the procedure code a direct reference to the programming element underlying the argument in the calling code.  
  
 If the underlying element in the calling code is a modifiable element and the argument is passed `ByRef`, the procedure code can use the direct reference to change the element's value in the calling code.  
  
## Changing the Underlying Value  
  
#### To change the underlying value of a procedure argument in the calling code  
  
1.  In the procedure declaration, specify [ByRef](../vs140/ByRef--Visual-Basic-.md) for the parameter corresponding to the argument.  
  
2.  In the calling code, pass a modifiable programming element as the argument.  
  
3.  In the calling code, do not enclose the argument in parentheses in the argument list.  
  
4.  In the procedure code, use the parameter name to assign a value to the underlying element in the calling code.  
  
 See the example further down for a demonstration.  
  
## Changing Local Copies  
 If the underlying element in the calling code is a nonmodifiable element, or if the argument is passed `ByVal`, the procedure cannot change its value in the calling code. However, the procedure can change its local copy of such an argument.  
  
#### To change the copy of a procedure argument in the procedure code  
  
1.  In the procedure declaration, specify [ByVal](../vs140/ByVal--Visual-Basic-.md) for the parameter corresponding to the argument.  
  
     -or-  
  
     In the calling code, enclose the argument in parentheses in the argument list. This forces [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] to pass the argument by value, even if the corresponding parameter specifies `ByRef`.  
  
2.  In the procedure code, use the parameter name to assign a value to the local copy of the argument. The underlying value in the calling code is not changed.  
  
## Example  
 The following example shows two procedures that take an array variable and operate on its elements. The `increase` procedure simply adds one to each element. The `replace` procedure assigns a new array to the parameter `a()` and then adds one to each element.  
  
 [!CODE [VbVbcnProcedures#35](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnProcedures#35)]  
  
 [!CODE [VbVbcnProcedures#36](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnProcedures#36)]  
  
 [!CODE [VbVbcnProcedures#37](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnProcedures#37)]  
  
 The first `MsgBox` call displays "After increase(n): 11, 21, 31, 41". Because the array `n` is a reference type, `replace` can change its members, even though the passing mechanism is `ByVal`.  
  
 The second `MsgBox` call displays "After replace(n): 101, 201, 301". Because `n` is passed `ByRef`, `replace` can modify the variable `n` in the calling code and assign a new array to it. Because `n` is a reference type, `replace` can also change its members.  
  
 You can prevent the procedure from modifying the variable itself in the calling code. See [How to: Protect a Procedure Argument Against Value Changes](../vs140/How-to--Protect-a-Procedure-Argument-Against-Value-Changes--Visual-Basic-.md).  
  
## Compiling the Code  
 When you pass a variable by reference, you must use the `ByRef` keyword to specify this mechanism.  
  
 The default in [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] is to pass arguments by value. However, it is good programming practice to include either the [ByVal](../vs140/ByVal--Visual-Basic-.md) or [ByRef](../vs140/ByRef--Visual-Basic-.md) keyword with every declared parameter. This makes your code easier to read.  
  
## .NET Framework Security  
 There is always a potential risk in allowing a procedure to change the value underlying an argument in the calling code. Make sure you expect this value to be changed, and be prepared to check it for validity before using it.  
  
## See Also  
 [Procedures in Visual Basic](../vs140/Procedures-in-Visual-Basic.md)   
 [Procedure Parameters and Arguments](../vs140/Procedure-Parameters-and-Arguments--Visual-Basic-.md)   
 [How to: Pass Arguments to a Procedure](../Topic/How%20to:%20Pass%20Arguments%20to%20a%20Procedure%20\(Visual%20Basic\).md)   
 [Argument Passing By Value and By Reference](../vs140/Passing-Arguments-by-Value-and-by-Reference--Visual-Basic-.md)   
 [Differences Between Modifiable and Nonmodifiable Arguments](../vs140/Differences-Between-Modifiable-and-Nonmodifiable-Arguments--Visual-Basic-.md)   
 [Differences Between Passing an Argument By Value and By Reference](../vs140/Differences-Between-Passing-an-Argument-By-Value-and-By-Reference--Visual-Basic-.md)   
 [How to: Protect a Procedure Argument Against Value Changes](../vs140/How-to--Protect-a-Procedure-Argument-Against-Value-Changes--Visual-Basic-.md)   
 [How to: Force an Argument to Be Passed by Value](../vs140/How-to--Force-an-Argument-to-Be-Passed-by-Value--Visual-Basic-.md)   
 [Argument Passing by Position and by Name](../vs140/Passing-Arguments-by-Position-and-by-Name--Visual-Basic-.md)   
 [Value Types and Reference Types](../Topic/Value%20Types%20and%20Reference%20Types.md)