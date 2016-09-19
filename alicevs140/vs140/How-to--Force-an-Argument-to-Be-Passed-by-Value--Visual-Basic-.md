---
title: "How to: Force an Argument to Be Passed by Value (Visual Basic)"
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
ms.assetid: 77b4f2d2-1055-4c2f-a521-874d1db86946
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Force an Argument to Be Passed by Value (Visual Basic)
The procedure declaration determines the passing mechanism. If a parameter is declared [ByRef](../vs140/ByRef--Visual-Basic-.md), [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] expects to pass the corresponding argument by reference. This allows the procedure to change the value of the programming element underlying the argument in the calling code. If you wish to protect the underlying element against such change, you can override the `ByRef` passing mechanism in the procedure call by enclosing the argument name in parentheses. These parentheses are in addition to the parentheses enclosing the argument list in the call.  
  
 The calling code cannot override a [ByVal](../vs140/ByVal--Visual-Basic-.md) mechanism.  
  
### To force an argument to be passed by value  
  
-   If the corresponding parameter is declared `ByVal` in the procedure, you do not need to take any additional steps. [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] already expects to pass the argument by value.  
  
-   If the corresponding parameter is declared `ByRef` in the procedure, enclose the argument in parentheses in the procedure call.  
  
## Example  
 The following example overrides a `ByRef` parameter declaration. In the call that forces `ByVal`, note the two levels of parentheses.  
  
 [!CODE [VbVbcnProcedures#39](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnProcedures#39)]  
  
 [!CODE [VbVbcnProcedures#40](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnProcedures#40)]  
  
 When `str` is enclosed in extra parentheses within the argument list, the `setNewString` procedure cannot change its value in the calling code, and `MsgBox` displays "Cannot be replaced if passed ByVal". When `str` is not enclosed in extra parentheses, the procedure can change it, and `MsgBox` displays "This is a new value for the inString argument."  
  
## Compiling the Code  
 When you pass a variable by reference, you must use the `ByRef` keyword to specify this mechanism.  
  
 The default in [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] is to pass arguments by value. However, it is good programming practice to include either the [ByVal](../vs140/ByVal--Visual-Basic-.md) or [ByRef](../vs140/ByRef--Visual-Basic-.md) keyword with every declared parameter. This makes your code easier to read.  
  
## Robust Programming  
 If a procedure declares a parameter [ByRef](../vs140/ByRef--Visual-Basic-.md), the correct execution of the code might depend on being able to change the underlying element in the calling code. If the calling code overrides this calling mechanism by enclosing the argument in parentheses, or if it passes a nonmodifiable argument, the procedure cannot change the underlying element. This might produce unexpected results in the calling code.  
  
## .NET Framework Security  
 There is always a potential risk in allowing a procedure to change the value underlying an argument in the calling code. Make sure you expect this value to be changed, and be prepared to check it for validity before using it.  
  
## See Also  
 [Procedures in Visual Basic](../vs140/Procedures-in-Visual-Basic.md)   
 [Procedure Parameters and Arguments](../vs140/Procedure-Parameters-and-Arguments--Visual-Basic-.md)   
 [How to: Pass Arguments to a Procedure](../Topic/How%20to:%20Pass%20Arguments%20to%20a%20Procedure%20\(Visual%20Basic\).md)   
 [Argument Passing By Value and By Reference](../vs140/Passing-Arguments-by-Value-and-by-Reference--Visual-Basic-.md)   
 [Differences Between Modifiable and Nonmodifiable Arguments](../vs140/Differences-Between-Modifiable-and-Nonmodifiable-Arguments--Visual-Basic-.md)   
 [Differences Between Passing an Argument By Value and By Reference](../vs140/Differences-Between-Passing-an-Argument-By-Value-and-By-Reference--Visual-Basic-.md)   
 [How to: Change the Value of a Procedure Argument](../vs140/How-to--Change-the-Value-of-a-Procedure-Argument--Visual-Basic-.md)   
 [How to: Protect a Procedure Argument Against Value Changes](../vs140/How-to--Protect-a-Procedure-Argument-Against-Value-Changes--Visual-Basic-.md)   
 [Argument Passing by Position and by Name](../vs140/Passing-Arguments-by-Position-and-by-Name--Visual-Basic-.md)   
 [Value Types and Reference Types](../Topic/Value%20Types%20and%20Reference%20Types.md)