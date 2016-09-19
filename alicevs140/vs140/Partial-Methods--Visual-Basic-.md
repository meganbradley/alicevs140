---
title: "Partial Methods (Visual Basic)"
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
ms.assetid: 74b3368b-b348-44a0-a326-7d7dc646f4e9
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Partial Methods (Visual Basic)
Partial methods enable developers to insert custom logic into code. Typically, the code is part of a designer-generated class. Partial methods are defined in a partial class that is created by a code generator, and they are commonly used to provide notification that something has been changed. They enable the developer to specify custom behavior in response to the change.  
  
 The designer of the code generator defines only the method signature and one or more calls to the method. Developers can then provide implementations for the method if they want to customize the behavior of the generated code. When no implementation is provided, calls to the method are removed by the compiler, resulting in no additional performance overhead.  
  
## Declaration  
 The generated code marks the definition of a partial method by placing the keyword `Partial` at the start of the signature line.  
  
```vb#  
Partial Private Sub QuantityChanged()  
End Sub  
```  
  
 The definition must meet the following conditions:  
  
-   The method must be a `Sub`, not a `Function`.  
  
-   The body of the method must be left empty.  
  
-   The access modifier must be `Private`.  
  
## Implementation  
 The implementation consists primarily of filling in the body of the partial method. The implementation is typically in a separate partial class from the definition, and is written by a developer who wants to extend the generated code.  
  
```vb#  
Private Sub QuantityChanged()  
'    Code for executing the desired action.  
End Sub  
```  
  
 The previous example duplicates the signature in the declaration exactly, but variations are possible. In particular, other modifiers can be added, such as `Overloads` or `Overrides`. Only one `Overrides` modifier is permitted. For more information about method modifiers, see [Sub Statement](../Topic/Sub%20Statement%20\(Visual%20Basic\).md).  
  
## Use  
 You call a partial method as you would call any other `Sub` procedure. If the method has been implemented, the arguments are evaluated and the body of the method is executed. However, remember that implementing a partial method is optional. If the method is not implemented, a call to it has no effect, and expressions passed as arguments to the method are not evaluated.  
  
## Example  
 In a file named Product.Designer.vb, define a `Product` class that has a `Quantity` property.  
  
 [!CODE [VbVbalrPartialMeths#4](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrPartialMeths#4)]  
  
 In a file named Product.vb, provide an implementation for `QuantityChanged`.  
  
 [!CODE [VbVbalrPartialMeths#5](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrPartialMeths#5)]  
  
 Finally, in the Main method of a project, declare a `Product` instance and provide an initial value for its `Quantity` property.  
  
 [!CODE [VbVbalrPartialMeths#6](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrPartialMeths#6)]  
  
 A message box should appear that displays this message:  
  
 `Quantity was changed to 100`  
  
## See Also  
 [Sub Statement](../Topic/Sub%20Statement%20\(Visual%20Basic\).md)   
 [Sub Procedure](../vs140/Sub-Procedures--Visual-Basic-.md)   
 [Optional Parameters](../vs140/Optional-Parameters--Visual-Basic-.md)   
 [Partial](../Topic/Partial%20\(Visual%20Basic\).md)   
 [Code Generation in LINQ to SQL](assetId:///ddcbdaa1-e7fa-4d85-a379-313b49965c07)   
 [How to: Override Default Methods](assetId:///3a73991e-fd4e-4610-93fb-7ced4dc6b7f9)