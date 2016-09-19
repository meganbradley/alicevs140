---
title: "Nothing and Strings in Visual Basic"
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
ms.assetid: 261380af-2024-4ecf-823b-43b1034d92cd
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Nothing and Strings in Visual Basic
The [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] runtime and the [!INCLUDE[dnprdnshort](../vs140/includes/dnprdnshort_md.md)] evaluate `Nothing` differently when it comes to strings.  
  
## Visual Basic Runtime and the .NET Framework  
 Consider the following example:  
  
 [!CODE [VbVbalrStrings#47](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStrings#47)]  
  
 The [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] runtime usually evaluates `Nothing` as an empty string (""). The [!INCLUDE[dnprdnshort](../vs140/includes/dnprdnshort_md.md)] does not, however, and throws an exception whenever an attempt is made to perform a string operation on `Nothing`.  
  
## See Also  
 [Introduction to Strings in Visual Basic](../vs140/Introduction-to-Strings-in-Visual-Basic.md)