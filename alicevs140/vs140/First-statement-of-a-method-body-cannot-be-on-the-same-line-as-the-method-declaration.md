---
title: "First statement of a method body cannot be on the same line as the method declaration"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 27df3488-de77-499d-b9a6-08037d540cb0
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# First statement of a method body cannot be on the same line as the method declaration
A `Function`, `Sub`, `Get`, `Set`, or `Property` statement must be alone on a source code line.  
  
 **Error ID:** BC30040  
  
### To correct this error  
  
1.  Remove any line label preceding the procedure declaration.  
  
2.  Move any statement preceding the procedure declaration to a previous source code line.  
  
3.  Move any statement following the procedure declaration to a subsequent source code line.  
  
## See Also  
 [Procedures in Visual Basic](../vs140/Procedures-in-Visual-Basic.md)   
 [How to: Label Statements](../vs140/How-to--Label-Statements--Visual-Basic-.md)