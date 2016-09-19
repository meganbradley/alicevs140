---
title: "How to: Use Lambda Expressions in a Query (C# Programming Guide)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3cac4d25-d11f-4abd-9e7c-0f02e97ae06d
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Use Lambda Expressions in a Query (C# Programming Guide)
You do not use lambda expressions directly in query syntax, but you do use them in method calls, and query expressions can contain method calls. In fact, some query operations can only be expressed in method syntax. For more information about the difference between query syntax and method syntax, see [Query Syntax versus Method Syntax (LINQ)](../Topic/Query%20Syntax%20and%20Method%20Syntax%20in%20LINQ%20\(C%23\).md).  
  
## Example  
 The following example demonstrates how to use a lambda expression in a method-based query by using the <xref:System.Linq.Enumerable.Where?qualifyHint=True> standard query operator. Note that the <xref:System.Linq.Enumerable.Where?qualifyHint=False> method in this example has an input parameter of the delegate type <xref:System.Func`1?qualifyHint=False> and that delegate takes an integer as input and returns a Boolean. The lambda expression can be converted to that delegate. If this were a [!INCLUDE[vbtecdlinq](../vs140/includes/vbtecdlinq_md.md)] query that used the <xref:System.Linq.Queryable.Where?qualifyHint=True> method, the parameter type would be an `Expression<Func<int,bool>>` but the lambda expression would look exactly the same. For more information on the Expression type, see <xref:System.Linq.Expressions.Expression?qualifyHint=True>.  
  
 [!CODE [csProgGuideLINQ#1](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideLINQ#1)]  
  
## Example  
 The following example demonstrates how to use a lambda expression in a method call of a query expression. The lambda is necessary because the <xref:System.Linq.Enumerable.Sum?qualifyHint=False> standard query operator cannot be invoked by using query syntax.  
  
 The query first groups the students according to their grade level, as defined in the `GradeLevel` enum. Then for each group it adds the total scores for each student. This requires two `Sum` operations. The inner `Sum` calculates the total score for each student, and the outer `Sum` keeps a running, combined total for all students in the group.  
  
 [!CODE [csProgGuideLINQ#2](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideLINQ#2)]  
  
## Compiling the Code  
 To run this code, copy and paste the method into the `StudentClass` that is provided in [How to: Query a Collection of Objects (C# Programming Guide)](../vs140/How-to--Query-a-Collection-of-Objects--C#-Programming-Guide-.md) and call it from the `Main` method.  
  
## See Also  
 [Lambda Expressions (C# Programming Guide)](../Topic/Lambda%20Expressions%20\(C%23%20Programming%20Guide\).md)   
 [Expression Trees](../vs140/Expression-Trees--C#-and-Visual-Basic-.md)