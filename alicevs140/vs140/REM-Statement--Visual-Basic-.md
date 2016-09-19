---
title: "REM Statement (Visual Basic)"
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
ms.assetid: 34126d7f-e0f9-476d-91e6-b31b398615dc
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# REM Statement (Visual Basic)
Used to include explanatory remarks in the source code of a program.  
  
## Syntax  
  
```  
REM comment  
' comment  
```  
  
## Parts  
 `comment`  
 Optional. The text of any comment you want to include. A space is required between the `REM` keyword and `comment`.  
  
## Remarks  
 You can put a `REM` statement alone on a line, or you can put it on a line following another statement. The `REM` statement must be the last statement on the line. If it follows another statement, the `REM` must be separated from that statement by a space.  
  
 You can use a single quotation mark (`'`) instead of `REM`. This is true whether your comment follows another statement on the same line or sits alone on a line.  
  
> [!NOTE]
>  You cannot continue a `REM` statement by using a line-continuation sequence (`_`). Once a comment begins, the compiler does not examine the characters for special meaning. For a multiple-line comment, use another `REM` statement or a comment symbol (`'`) on each line.  
  
## Example  
 The following example illustrates the `REM` statement, which is used to include explanatory remarks in a program. It also shows the alternative of using the single quotation-mark character (`'`) instead of `REM`.  
  
 [!CODE [VbVbalrStatements#6](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStatements#6)]  
  
## See Also  
 [Comments in Code](../vs140/Comments-in-Code--Visual-Basic-.md)   
 [How to: Break and Combine Statements in Code](../vs140/How-to--Break-and-Combine-Statements-in-Code--Visual-Basic-.md)