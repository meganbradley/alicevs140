---
title: "Variables in Visual Basic"
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
ms.assetid: 4cfaa06d-4ae3-4307-897b-cf599dc24caa
caps.latest.revision: 29
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Variables in Visual Basic
You often have to store values when you perform calculations with [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)]. For example, you might want to calculate several values, compare them, and perform different operations on them, depending on the result of the comparison. You have to retain the values if you want to compare them.  
  
## Usage  
 [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)], just like most programming languages, uses variables for storing values. A *variable* has a name (the word that you use to refer to the value that the variable contains). A variable also has a data type (which determines the kind of data that the variable can store). A variable can represent an array if it has to store an indexed set of closely related data items.  
  
 Local type inference enables you to declare variables without explicitly stating a data type. Instead, the compiler infers the type of the variable from the type of the initialization expression. For more information, see [Local Type Inference](../vs140/Local-Type-Inference--Visual-Basic-.md) and [Option Infer Statement](../vs140/Option-Infer-Statement.md).  
  
## Assigning Values  
 You use assignment statements to perform calculations and assign the result to a variable, as the following example shows.  
  
 [!CODE [VbVbalrVariables#1](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrVariables#1)]  
  
> [!NOTE]
>  The equal sign (`=`) in this example is an assignment operator, not an equality operator. The value is being assigned to the variable `applesSold`.  
  
 For more information, see [How to: Move Data into and out of a Variable](../vs140/How-to--Move-Data-Into-and-Out-of-a-Variable--Visual-Basic-.md).  
  
## Variables and Properties  
 Like a variable, a *property* represents a value that you can access. However, it is more complex than a variable. A property uses code blocks that control how to set and retrieve its value. For more information, see [Differences Between Properties and Variables in Visual Basic](../vs140/Differences-Between-Properties-and-Variables-in-Visual-Basic.md).  
  
## See Also  
 [Variable Declaration](../Topic/Variable%20Declaration%20in%20Visual%20Basic.md)   
 [Object Variables](../Topic/Object%20Variables%20in%20Visual%20Basic.md)   
 [Troubleshooting Variables in Visual Basic](../Topic/Troubleshooting%20Variables%20in%20Visual%20Basic.md)   
 [How to: Move Data into and out of a Variable](../vs140/How-to--Move-Data-Into-and-Out-of-a-Variable--Visual-Basic-.md)   
 [Differences Between Properties and Variables in Visual Basic](../vs140/Differences-Between-Properties-and-Variables-in-Visual-Basic.md)   
 [Local Type Inference](../vs140/Local-Type-Inference--Visual-Basic-.md)