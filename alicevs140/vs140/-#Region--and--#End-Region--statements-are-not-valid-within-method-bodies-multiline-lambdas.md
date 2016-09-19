---
title: "&#39;#Region&#39; and &#39;#End Region&#39; statements are not valid within method bodies-multiline lambdas"
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
H1: &#39;#Region&#39; and &#39;#End Region&#39; statements are not valid within method bodies/multiline lambdas
ms.assetid: 43707bf1-1c6b-4d82-b081-e5a17dca51c1
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;#Region&#39; and &#39;#End Region&#39; statements are not valid within method bodies-multiline lambdas
The `#Region` block must be declared at a class, module, or namespace level. A collapsible region can include one or more procedures, but it cannot begin or end inside of a procedure.  
  
 **Error ID:** BC32025  
  
### To correct this error  
  
1.  Ensure that the preceding procedure is properly terminated with an `End Function` or `End Sub` statement.  
  
2.  Ensure that the `#Region` and `#End Region` directives are in the same code block.  
  
## See Also  
 [#Region Directive](../vs140/#Region-Directive.md)