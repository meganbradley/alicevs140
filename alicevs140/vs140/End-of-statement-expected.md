---
title: "End of statement expected"
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
ms.assetid: 53c7f825-a737-4b76-a1fa-f67745b8bd40
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# End of statement expected
The statement is syntactically complete, but an additional programming element follows the element that completes the statement. A line terminator is required at the end of every statement.  
  
 A line terminator divides the characters of a Visual Basic source file into lines. Examples of line terminators are the Unicode carriage return character (&HD), the Unicode linefeed character (&HA), and the Unicode carriage return character followed by the Unicode linefeed character. For more information about line terminators, see the [Visual Basic Language Specification](../vs140/Visual-Basic-Language-Specification.md).  
  
 **Error ID:** BC30205  
  
### To correct this error  
  
1.  Check to see if two different statements have inadvertently been put on the same line.  
  
2.  Insert a line terminator after the element that completes the statement.  
  
## See Also  
 [How to: Break and Combine Statements in Code](../vs140/How-to--Break-and-Combine-Statements-in-Code--Visual-Basic-.md)   
 [Statements](../vs140/Statements-in-Visual-Basic.md)