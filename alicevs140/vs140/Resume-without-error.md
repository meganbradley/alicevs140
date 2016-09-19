---
title: "Resume without error"
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
ms.assetid: f9631804-fd36-4443-b36c-30db827e6176
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Resume without error
A `Resume` statement appeared outside error-handling code, or the code jumped into an error handler even though there was no error.  
  
### To correct this error  
  
1.  Move the `Resume`statement into an error handler, or delete it.  
  
2.  Jumps to labels cannot occur across procedures, so search the procedure for the label that identifies the error handler. If you find a duplicate label specified as the target of a `GoTo` statement that isn't an `On Error GoTo` statement, change the line label to agree with its intended target.  
  
## See Also  
 [Resume Statement](../vs140/Resume-Statement.md)   
 [On Error Statement (Visual Basic)](../Topic/On%20Error%20Statement%20\(Visual%20Basic\).md)