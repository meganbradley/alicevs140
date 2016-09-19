---
title: "How to: Convert Hexadecimal Strings to Numbers (Visual Basic)"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - VB
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-visual-basic
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 76675807-eadb-4c08-bd50-e6c6ff4b8ced
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Convert Hexadecimal Strings to Numbers (Visual Basic)
This example converts a hexadecimal string to an integer using the <xref:System.Convert.ToInt32?qualifyHint=False> method.  
  
### To convert a hexadecimal string to a number  
  
-   Use the <xref:System.Convert.ToInt32?qualifyHint=False> method to convert the number expressed in base-16 to an integer.  
  
     The first argument of the <xref:System.Convert.ToInt32?qualifyHint=False> method is the string to convert. The second argument describes what base the number is expressed in; hexadecimal is base 16.  
  
     [!CODE [VbVbalrStrings#62](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStrings#62)]  
  
## See Also  
 <xref:Microsoft.VisualBasic.Conversion.Hex?qualifyHint=False>   
 <xref:System.Convert.ToInt32?qualifyHint=False>