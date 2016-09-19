---
title: "How to: Validate Strings That Represent Dates or Times (Visual Basic)"
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
ms.assetid: ae7d4b29-3436-4032-bdbf-4650eb1c8e19
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Validate Strings That Represent Dates or Times (Visual Basic)
The following code example sets a `Boolean` value that indicates whether a string represents a valid date or time.  
  
## Example  
 [!CODE [VbVbcnRegEx#2](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnRegEx#2)]  
  
## Compiling the Code  
 Replace `("01/01/03")` and `"9:30 PM"` with the date and time you want to validate. You can replace the string with another hard-coded string, with a `String` variable, or with a method that returns a string, such as `InputBox`.  
  
## Robust Programming  
 Use this method to validate the string before trying to convert the `String` to a `DateTime` variable. By checking the date or time first, you can avoid generating an exception at run time.  
  
## See Also  
 <xref:Microsoft.VisualBasic.Information.IsDate?qualifyHint=False>   
 <xref:Microsoft.VisualBasic.Interaction.InputBox?qualifyHint=False>   
 [Validating Strings in Visual Basic](../Topic/Validating%20Strings%20in%20Visual%20Basic.md)