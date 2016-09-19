---
title: "Passing Arguments by Position and by Name (Visual Basic)"
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
ms.assetid: 1ad7358f-1da9-48da-a95b-f3c7ed41eff3
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Passing Arguments by Position and by Name (Visual Basic)
When you call a `Sub` or `Function` procedure, you can pass arguments *by position* — in the order in which they appear in the procedure's definition — or you can pass them *by name*, without regard to position.  
  
 When you pass an argument by name, you specify the argument's declared name followed by a colon and an equal sign (`:=`), followed by the argument value. You can supply named arguments in any order.  
  
 For example, the following `Sub` procedure takes three arguments:  
  
 [!CODE [VbVbcnProcedures#41](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnProcedures#41)]  
  
 When you call this procedure, you can supply the arguments by position, by name, or by using a mixture of both.  
  
## Passing Arguments by Position  
 You can call the procedure `studentInfo` with its arguments passed by position and delimited by commas, as shown in the following example:  
  
 [!CODE [VbVbcnProcedures#42](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnProcedures#42)]  
  
 If you omit an optional argument in a positional argument list, you must hold its place with a comma. The following example calls `studentInfo` without the `age` argument:  
  
 [!CODE [VbVbcnProcedures#43](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnProcedures#43)]  
  
## Passing Arguments by Name  
 Alternatively, you can call `studentInfo` with the arguments passed by name, also delimited by commas, as shown in the following example:  
  
 [!CODE [VbVbcnProcedures#44](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnProcedures#44)]  
  
## Mixing Arguments by Position and by Name  
 You can supply arguments both by position and by name in a single procedure call, as shown in the following example:  
  
 [!CODE [VbVbcnProcedures#45](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnProcedures#45)]  
  
 In the preceding example, no extra comma is necessary to hold the place of the omitted `age` argument, since `birth` is passed by name.  
  
 When you supply arguments by a mixture of position and name, the positional arguments must all come first. Once you supply an argument by name, the remaining arguments must all be by name.  
  
## Supplying Optional Arguments by Name  
 Passing arguments by name is especially useful when you call a procedure that has more than one optional argument. If you supply arguments by name, you do not have to use consecutive commas to denote missing positional arguments. Passing arguments by name also makes it easier to keep track of which arguments you are passing and which ones you are omitting.  
  
## Restrictions on Supplying Arguments by Name  
 You cannot pass arguments by name to avoid entering required arguments. You can omit only the optional arguments.  
  
 You cannot pass a parameter array by name. This is because when you call the procedure, you supply an indefinite number of comma-separated arguments for the parameter array, and the compiler cannot associate more than one argument with a single name.  
  
## See Also  
 [Procedures in Visual Basic](../vs140/Procedures-in-Visual-Basic.md)   
 [Procedure Parameters and Arguments](../vs140/Procedure-Parameters-and-Arguments--Visual-Basic-.md)   
 [How to: Pass Arguments to a Procedure](../Topic/How%20to:%20Pass%20Arguments%20to%20a%20Procedure%20\(Visual%20Basic\).md)   
 [Argument Passing By Value and By Reference](../vs140/Passing-Arguments-by-Value-and-by-Reference--Visual-Basic-.md)   
 [Optional Parameters](../vs140/Optional-Parameters--Visual-Basic-.md)   
 [Parameter Arrays](../Topic/Parameter%20Arrays%20\(Visual%20Basic\).md)   
 [Optional](../vs140/Optional--Visual-Basic-.md)   
 [ParamArray](../vs140/ParamArray--Visual-Basic-.md)