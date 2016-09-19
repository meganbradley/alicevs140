---
title: "Erase Statement (Visual Basic)"
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
ms.assetid: 7a8133d7-b750-4d74-8b66-ba1dd9778d4b
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Erase Statement (Visual Basic)
Used to release array variables and deallocate the memory used for their elements.  
  
## Syntax  
  
```  
Erase arraylist  
```  
  
## Parts  
 `arraylist`  
 Required. List of array variables to be erased. Multiple variables are separated by commas.  
  
## Remarks  
 The `Erase` statement can appear only at procedure level. This means you can release arrays inside a procedure but not at class or module level.  
  
 The `Erase` statement is equivalent to assigning `Nothing` to each array variable.  
  
## Example  
 The following example uses the `Erase` statement to clear two arrays and free their memory (1000 and 100 storage elements, respectively). The `ReDim` statement then assigns a new array instance to the three-dimensional array.  
  
 [!CODE [VbVbalrStatements#19](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStatements#19)]  
  
## See Also  
 [Nothing](../Topic/Nothing%20\(Visual%20Basic\).md)   
 [ReDim Statement](../vs140/ReDim-Statement--Visual-Basic-.md)