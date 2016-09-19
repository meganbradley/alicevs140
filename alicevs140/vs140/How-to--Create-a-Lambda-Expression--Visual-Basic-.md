---
title: "How to: Create a Lambda Expression (Visual Basic)"
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
ms.assetid: 3279bd5c-80f7-410a-a7ba-f7085ed36aa5
caps.latest.revision: 29
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Create a Lambda Expression (Visual Basic)
A *lambda expression* is a function or subroutine that does not have a name. A lambda expression can be used wherever a delegate type is valid.  
  
### To create a single-line lambda expression function  
  
1.  In any situation where a delegate type could be used, type the keyword `Function`, as in the following example:  
  
     `Dim add1 =`   `Function`  
  
2.  In parentheses, directly after `Function`, type the parameters of the function. Notice that you do not specify a name after `Function`.  
  
     `Dim add1 = Function`   `(num As Integer)`  
  
3.  Following the parameter list, type a single expression as the body of the function. The value that the expression evaluates to is the value returned by the function. You do not use an `As` clause to specify the return type.  
  
     [!CODE [VbVbalrLambdas#1](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrLambdas#1)]  
  
     You call the lambda expression by passing in an integer argument.  
  
     [!CODE [VbVbalrLambdas#2](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrLambdas#2)]  
  
4.  Alternatively, the same result is accomplished by the following example:  
  
     [!CODE [VbVbalrLambdas#3](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrLambdas#3)]  
  
### To create a single-line lambda expression subroutine  
  
1.  In any situation where a delegate type could be used, type the keyword `Sub`, as shown in the following example.  
  
     `Dim add1 =`   `Sub`  
  
2.  In parentheses, directly after `Sub`, type the parameters of the subroutine. Notice that you do not specify a name after `Sub`.  
  
     `Dim add1 = Sub`   `(msg As String)`  
  
3.  Following the parameter list, type a single statement as the body of the subroutine.  
  
     [!CODE [VbVbalrLambdas#17](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrLambdas#17)]  
  
     You call the lambda expression by passing in a string argument.  
  
     [!CODE [VbVbalrLambdas#18](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrLambdas#18)]  
  
### To create a multiline lambda expression function  
  
1.  In any situation where a delegate type could be used, type the keyword `Function`, as shown in the following example.  
  
     `Dim add1 =`   `Function`  
  
2.  In parentheses, directly after `Function`, type the parameters of the function. Notice that you do not specify a name after `Function`.  
  
     `Dim add1 = Function`   `(index As Integer)`  
  
3.  Press ENTER. The `End Function` statement is automatically added.  
  
4.  Within the body of the function, add the following code to create an expression and return the value. You do not use an `As` clause to specify the return type.  
  
     [!CODE [VbVbalrLambdas#19](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrLambdas#19)]  
  
     You call the lambda expression by passing in an integer argument.  
  
     [!CODE [VbVbalrLambdas#20](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrLambdas#20)]  
  
### To create a multiline lambda expression subroutine  
  
1.  In any situation where a delegate type could be used, type the keyword `Sub`, as shown in the following example:  
  
     `Dim add1 =`   `Sub`  
  
2.  In parentheses, directly after `Sub`, type the parameters of the subroutine. Notice that you do not specify a name after `Sub`.  
  
     `Dim add1 = Sub`  `(msg As String)`  
  
3.  Press ENTER. The `End Sub` statement is automatically added.  
  
4.  Within the body of the function, add the following code to execute when the subroutine is invoked.  
  
     [!CODE [VbVbalrLambdas#21](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrLambdas#21)]  
  
     You call the lambda expression by passing in a string argument.  
  
     [!CODE [VbVbalrLambdas#22](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrLambdas#22)]  
  
## Example  
 A common use of lambda expressions is to define a function that can be passed in as the argument for a parameter whose type is `Delegate`. In the following example, the <xref:System.Diagnostics.Process.GetProcesses?qualifyHint=False> method returns an array of the processes running on the local computer. The <xref:System.Linq.Enumerable.Where``1?qualifyHint=False> method from the <xref:System.Linq.Enumerable?qualifyHint=False> class requires a `Boolean` delegate as its argument. The lambda expression in the example is used for that purpose. It returns `True` for each process that has only one thread, and those are selected in `filteredList`.  
  
 [!CODE [VbVbalrLambdas#10](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrLambdas#10)]  
  
 The previous example is equivalent to the following code, which is written in [!INCLUDE[vbteclinqext](../vs140/includes/vbteclinqext_md.md)] syntax:  
  
 [!CODE [VbVbalrLambdas#11](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrLambdas#11)]  
  
## See Also  
 <xref:System.Linq.Enumerable?qualifyHint=False>   
 [Lambda Expressions](../vs140/Lambda-Expressions--Visual-Basic-.md)   
 [Function Statement](../Topic/Function%20Statement%20\(Visual%20Basic\).md)   
 [Sub Statement (Visual Basic)](../Topic/Sub%20Statement%20\(Visual%20Basic\).md)   
 [Delegates (Visual Basic)](../Topic/Delegates%20\(Visual%20Basic\).md)   
 [How to: Pass Procedures to Another Procedure in Visual Basic](../vs140/How-to--Pass-Procedures-to-Another-Procedure-in-Visual-Basic.md)   
 [Delegate Statement](../vs140/Delegate-Statement.md)   
 [Introduction to LINQ in Visual Basic](../Topic/Introduction%20to%20LINQ%20in%20Visual%20Basic.md)