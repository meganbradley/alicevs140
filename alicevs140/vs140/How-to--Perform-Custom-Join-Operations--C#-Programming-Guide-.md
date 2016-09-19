---
title: "How to: Perform Custom Join Operations (C# Programming Guide)"
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
ms.assetid: a05e2ab1-410d-4a1d-8ada-af93539682c9
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Perform Custom Join Operations (C# Programming Guide)
This example shows how to perform join operations that are not possible with the `join` clause. In a query expression, the `join` clause is limited to, and optimized for, equijoins, which are by far the most common type of join operation. When performing an equijoin, you will probably always get the best performance by using the `join` clause.  
  
 However, the `join` clause cannot be used in the following cases:  
  
-   When the join is predicated on an expression of inequality (a non-equijoin).  
  
-   When the join is predicated on more than one expression of equality or inequality.  
  
-   When you have to introduce a temporary range variable for the right side (inner) sequence before the join operation.  
  
 To perform joins that are not equijoins, you can use multiple `from` clauses to introduce each data source independently. You then apply a predicate expression in a `where` clause to the range variable for each source. The expression also can take the form of a method call.  
  
> [!NOTE]
>  Do not confuse this kind of custom join operation with the use of multiple `from` clauses to access inner collections. For more information, see [join clause (C# Reference)](../Topic/join%20clause%20\(C%23%20Reference\).md).  
  
## Example  
 The first method in the following example shows a simple cross join. Cross joins must be used with caution because they can produce very large result sets. However, they can be useful in some scenarios for creating source sequences against which additional queries are run.  
  
 The second method produces a sequence of all the products whose category ID is listed in the category list on the left side. Note the use of the `let` clause and the `Contains` method to create a temporary array. It also is possible to create the array before the query and eliminate the first `from` clause.  
  
 [!CODE [csProgGuideLINQ#64](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideLINQ#64)]  
  
## Example  
 In the following example, the query must join two sequences based on matching keys that, in the case of the inner (right side) sequence, cannot be obtained prior to the join clause itself. If this join were performed with a `join` clause, then the `Split` method would have to be called for each element. The use of multiple `from` clauses enables the query to avoid the overhead of the repeated method call. However, since `join` is optimized, in this particular case it might still be faster than using multiple `from` clauses. The results will vary depending primarily on how expensive the method call is.  
  
 [!CODE [csProgGuideLINQ#13](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideLINQ#13)]  
  
## Compiling the Code  
  
-   Create a [!INCLUDE[vs_current_short](../vs140/includes/vs_current_short_md.md)] console application project that targets [!INCLUDE[dnprdnshort](../vs140/includes/dnprdnshort_md.md)] 3.5 or later. By default, the project has a reference to System.Core.dll and a `using` directive for the System.Linq namespace.  
  
-   Replace the `Program` class with the code in the previous example.  
  
-   Follow the instructions in [How To: Join Content from Dissimilar Files (LINQ)](../vs140/How-to--Join-Content-from-Dissimilar-Files--LINQ-.md) to set up the data files, scores.csv and names.csv.  
  
-   Press F5 to compile and run the program.  
  
-   Press any key to exit the console window.  
  
## See Also  
 [LINQ Query Expressions (C# Programming Guide)](../Topic/LINQ%20Query%20Expressions%20\(C%23%20Programming%20Guide\).md)   
 [join clause (C# Reference)](../Topic/join%20clause%20\(C%23%20Reference\).md)   
 [Join Operations](../vs140/Join-Operations.md)   
 [How to: Order the Results of a Join Clause (C# Programming Guide)](../vs140/How-to--Order-the-Results-of-a-Join-Clause--C#-Programming-Guide-.md)