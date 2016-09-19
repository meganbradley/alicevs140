---
title: "Differences Between Passing an Argument By Value and By Reference (Visual Basic)"
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
ms.assetid: 5f5c38fe-3e2d-494c-8fff-f4025b55ec93
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Differences Between Passing an Argument By Value and By Reference (Visual Basic)
When you pass one or more arguments to a procedure, each argument corresponds to an underlying programming element in the calling code. You can pass either the value of this underlying element, or a reference to it. This is known as the *passing mechanism*.  
  
## Passing by Value  
 You pass an argument *by value* by specifying the [ByVal](../vs140/ByVal--Visual-Basic-.md) keyword for the corresponding parameter in the procedure definition. When you use this passing mechanism, [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] copies the value of the underlying programming element into a local variable in the procedure. The procedure code does not have any access to the underlying element in the calling code.  
  
## Passing by Reference  
 You pass an argument *by reference* by specifying the [ByRef](../vs140/ByRef--Visual-Basic-.md) keyword for the corresponding parameter in the procedure definition. When you use this passing mechanism, [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] gives the procedure a direct reference to the underlying programming element in the calling code.  
  
## Passing Mechanism and Element Type  
 The choice of passing mechanism is not the same as the classification of the underlying element type. Passing by value or by reference refers to what [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] supplies to the procedure code. A value type or reference type refers to how a programming element is stored in memory.  
  
 However, the passing mechanism and element type are interrelated. The value of a reference type is a pointer to the data elsewhere in memory. This means that when you pass a reference type by value, the procedure code has a pointer to the underlying element's data, even though it cannot access the underlying element itself. For example, if the element is an array variable, the procedure code does not have access to the variable itself, but it can access the array members.  
  
## Ability to Modify  
 When you pass a nonmodifiable element as an argument, the procedure can never modify it in the calling code, whether it is passed `ByVal` or `ByRef`.  
  
 For a modifiable element, the following table summarizes the interaction between the element type and the passing mechanism.  
  
|Element type|Passed `ByVal`|Passed `ByRef`|  
|------------------|--------------------|--------------------|  
|Value type (contains only a value)|The procedure cannot change the variable or any of its members.|The procedure can change the variable and its members.|  
|Reference type (contains a pointer to a class or structure instance)|The procedure cannot change the variable but can change members of the instance to which it points.|The procedure can change the variable and members of the instance to which it points.|  
  
## See Also  
 [Procedures in Visual Basic](../vs140/Procedures-in-Visual-Basic.md)   
 [Procedure Parameters and Arguments](../vs140/Procedure-Parameters-and-Arguments--Visual-Basic-.md)   
 [How to: Pass Arguments to a Procedure](../Topic/How%20to:%20Pass%20Arguments%20to%20a%20Procedure%20\(Visual%20Basic\).md)   
 [Argument Passing By Value and By Reference](../vs140/Passing-Arguments-by-Value-and-by-Reference--Visual-Basic-.md)   
 [Differences Between Modifiable and Nonmodifiable Arguments](../vs140/Differences-Between-Modifiable-and-Nonmodifiable-Arguments--Visual-Basic-.md)   
 [How to: Change the Value of a Procedure Argument](../vs140/How-to--Change-the-Value-of-a-Procedure-Argument--Visual-Basic-.md)   
 [How to: Protect a Procedure Argument Against Value Changes](../vs140/How-to--Protect-a-Procedure-Argument-Against-Value-Changes--Visual-Basic-.md)   
 [How to: Force an Argument to Be Passed by Value](../vs140/How-to--Force-an-Argument-to-Be-Passed-by-Value--Visual-Basic-.md)   
 [Argument Passing by Position and by Name](../vs140/Passing-Arguments-by-Position-and-by-Name--Visual-Basic-.md)   
 [Value Types and Reference Types](../Topic/Value%20Types%20and%20Reference%20Types.md)