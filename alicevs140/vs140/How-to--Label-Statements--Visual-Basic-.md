---
title: "How to: Label Statements (Visual Basic)"
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
ms.assetid: 38f1ff43-2054-42cb-963b-1998e60c6ed4
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Label Statements (Visual Basic)
Statement blocks are made up of lines of code delimited by colons. Lines of code preceded by an identifying string or integer are said to be *labeled*. Statement labels are used to mark a line of code to identify it for use with statements such as `On Error Goto`.  
  
 Labels may be either valid Visual Basic identifiers—such as those that identify programming elements—or integer literals. A label must appear at the beginning of a line of source code and must be followed by a colon, regardless of whether it is followed by a statement on the same line.  
  
 The compiler identifies labels by checking whether the beginning of the line matches any already-defined identifier. If it does not, the compiler assumes it is a label.  
  
 Labels have their own declaration space and do not interfere with other identifiers. A label's scope is the body of the method. Label declaration takes precedence in any ambiguous situation.  
  
> [!NOTE]
>  Labels can be used only on executable statements inside methods.  
  
### To label a line of code  
  
-   Place an identifier, followed by a colon, at the beginning of the line of source code.  
  
     For example, the following lines of code are labeled with `Jump` and `120`, respectively:  
  
     [!CODE [VbVbalrStatements#708](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrStatements#708)]  
  
## See Also  
 [Statements in Visual Basic](../vs140/Statements-in-Visual-Basic.md)   
 [Declared Element Names](../vs140/Declared-Element-Names--Visual-Basic-.md)   
 [Program Structure and Code Conventions](../vs140/Program-Structure-and-Code-Conventions--Visual-Basic-.md)