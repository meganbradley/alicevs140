---
title: "How to: Create a String from An Array of Char Values (Visual Basic)"
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
ms.assetid: 69f94e85-d57c-4ccc-a62a-426e829f5c5e
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Create a String from An Array of Char Values (Visual Basic)
This example creates the string "abcd" from individual characters.  
  
## Example  
 [!CODE [VbVbalrStrings#61](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStrings#61)]  
  
## Compiling the Code  
 This method has no special requirements.  
  
 The syntax `"a"c`, where a single `c` follows a single character in quotation marks, is used to create a character literal.  
  
## Robust Programming  
 Null characters (equivalent to `Chr(0)`) in the string lead to unexpected results when using the string. The null character will be included with the string, but characters following the null character will not be displayed in some situations.  
  
## See Also  
 <xref:System.String?qualifyHint=False>   
 [Char Data Type](../vs140/Char-Data-Type--Visual-Basic-.md)   
 [Data Types](../vs140/Data-Types-in-Visual-Basic.md)