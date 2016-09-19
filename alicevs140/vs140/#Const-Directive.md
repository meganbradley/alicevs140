---
title: "#Const Directive"
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
ms.assetid: 707669e5-23f9-4f17-8622-a0d534429386
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# #Const Directive
Defines conditional compiler constants for Visual Basic.  
  
## Syntax  
  
```  
#Const constname = expression  
```  
  
## Parts  
 `constname`  
 Required. Name of the constant being defined.  
  
 `expression`  
 Required. Literal, other conditional compiler constant, or any combination that includes any or all arithmetic or logical operators except `Is`.  
  
## Remarks  
 Conditional compiler constants are always private to the file in which they appear. You cannot create public compiler constants using the `#Const` directive; you can create them only in the user interface or with the `/define` compiler option.  
  
 You can use only conditional compiler constants and literals in `expression`. Using a standard constant defined with `Const` causes an error. Conversely, you can use constants defined with the `#Const` keyword only for conditional compilation. Constants can also be undefined, in which case they have a value of `Nothing`.  
  
## Example  
 This example uses the `#Const` directive.  
  
 [!CODE [VbVbalrConditionalComp#3](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrConditionalComp#3)]  
  
## See Also  
 [/define (Visual Basic)](../vs140/-define--Visual-Basic-.md)   
 [#If...Then...#Else Directives](../vs140/#If...Then...#Else-Directives.md)   
 [Const Statement](../Topic/Const%20Statement%20\(Visual%20Basic\).md)   
 [Conditional Compilation in Visual Basic](../vs140/Conditional-Compilation-in-Visual-Basic.md)   
 [If...Then...Else Statement (Visual Basic)](../Topic/If...Then...Else%20Statement%20\(Visual%20Basic\).md)