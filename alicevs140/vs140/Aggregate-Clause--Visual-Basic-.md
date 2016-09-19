---
title: "Aggregate Clause (Visual Basic)"
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
ms.assetid: 1315a814-5db6-4077-b34b-b141e11cc0eb
caps.latest.revision: 27
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Aggregate Clause (Visual Basic)
Applies one or more aggregate functions to a collection.  
  
## Syntax  
  
```  
Aggregate element [As type] In collection _  
  [, element2 [As type2] In collection2, [...]]  
  [ clause ]  
  Into expressionList  
```  
  
## Parts  
  
|||  
|-|-|  
|Term|Definition|  
|`element`|Required. Variable used to iterate through the elements of the collection.|  
|`type`|Optional. The type of `element`. If no type is specified, the type of `element` is inferred from `collection`.|  
|`collection`|Required. Refers to the collection to operate on.|  
|`clause`|Optional. One or more query clauses, such as a `Where` clause, to refine the query result to apply the aggregate clause or clauses to.|  
|`expressionList`|Required. One or more comma-delimited expressions that identify an aggregate function to apply to the collection. You can apply an alias to an aggregate function to specify a member name for the query result. If no alias is supplied, the name of the aggregate function is used. For examples, see the section about aggregate functions later in this topic.|  
  
## Remarks  
 The `Aggregate` clause can be used to include aggregate functions in your queries. Aggregate functions perform checks and computations over a set of values and return a single value. You can access the computed value by using a member of the query result type. The standard aggregate functions that you can use are the `All`, `Any`, `Average`, `Count`, `LongCount`, `Max`, `Min`, and `Sum` functions. These functions are familiar to developers who are familiar with aggregates in SQL. They are described in the following section of this topic.  
  
 The result of an aggregate function is included in the query result as a field of the query result type. You can supply an alias for the aggregate function result to specify the name of the member of the query result type that will hold the aggregate value. If no alias is supplied, the name of the aggregate function is used.  
  
 The `Aggregate` clause can begin a query, or it can be included as an additional clause in a query. If the `Aggregate` clause begins a query, the result is a single value that is the result of the aggregate function specified in the `Into` clause. If more than one aggregate function is specified in the `Into` clause, the query returns a single type with a separate property to reference the result of each aggregate function in the `Into` clause. If the `Aggregate` clause is included as an additional clause in a query, the type returned in the query collection will have a separate property to reference the result of each aggregate function in the `Into` clause.  
  
## Aggregate Functions  
 The following list describes the standard aggregate functions that can be used with the `Aggregate` clause.  
  
|||  
|-|-|  
|Function|Description|  
|`All`|Returns `true` if all elements in the collection satisfy a specified condition; otherwise returns `false`. Following is an example:<br /><br /> [!CODE [VbSimpleQuerySamples#5](../CodeSnippet/VS_Snippets_VBCSharp/VbSimpleQuerySamples#5)]|  
|`Any`|Returns `true` if any element in the collection satisfies a specified condition; otherwise returns `false`. Following is an example:<br /><br /> [!CODE [VbSimpleQuerySamples#6](../CodeSnippet/VS_Snippets_VBCSharp/VbSimpleQuerySamples#6)]|  
|`Average`|Computes the average of all elements in the collection, or a computes supplied expression for all elements in the collection. Following is an example:<br /><br /> [!CODE [VbSimpleQuerySamples#7](../CodeSnippet/VS_Snippets_VBCSharp/VbSimpleQuerySamples#7)]|  
|`Count`|Counts the number of elements in the collection. You can supply an optional `Boolean` expression to count only the number of elements in the collection that satisfy a condition. Following is an example:<br /><br /> [!CODE [VbSimpleQuerySamples#8](../CodeSnippet/VS_Snippets_VBCSharp/VbSimpleQuerySamples#8)]|  
|`Group`|Refers to query results that are grouped as a result of a `Group By` or `Group Join` clause. The `Group` function is valid only in the `Into` clause of a `Group By` or `Group Join` clause. For more information and examples, see [Group By Clause (Visual Basic)](../vs140/Group-By-Clause--Visual-Basic-.md) and [Group Join Clause (Visual Basic)](../vs140/Group-Join-Clause--Visual-Basic-.md).|  
|`LongCount`|Counts the number of elements in the collection. You can supply an optional `Boolean` expression to count only the number of elements in the collection that satisfy a condition. Returns the result as a `Long`. For an example, see the `Count` aggregate function.|  
|`Max`|Computes the maximum value from the collection, or computes a supplied expression for all elements in the collection. Following is an example:<br /><br /> [!CODE [VbSimpleQuerySamples#9](../CodeSnippet/VS_Snippets_VBCSharp/VbSimpleQuerySamples#9)]|  
|`Min`|Computes the minimum value from the collection, or computes a supplied expression for all elements in the collection. Following is an example:<br /><br /> [!CODE [VbSimpleQuerySamples#10](../CodeSnippet/VS_Snippets_VBCSharp/VbSimpleQuerySamples#10)]|  
|`Sum`|Computes the sum of all elements in the collection, or computes a supplied expression for all elements in the collection. Following is an example:<br /><br /> [!CODE [VbSimpleQuerySamples#15](../CodeSnippet/VS_Snippets_VBCSharp/VbSimpleQuerySamples#15)]|  
  
## Example  
 The following code example shows how to use the `Aggregate` clause to apply aggregate functions to a query result.  
  
 [!CODE [VbSimpleQuerySamples#4](../CodeSnippet/VS_Snippets_VBCSharp/VbSimpleQuerySamples#4)]  
  
## Creating User-Defined Aggregate Functions  
 You can include your own custom aggregate functions in a query expression by adding extension methods to the <xref:System.Collections.Generic.IEnumerable`1?qualifyHint=False> type. Your custom method can then perform a calculation or operation on the enumerable collection that has referenced your aggregate function. For more information about extension methods, see [Extension Methods (Visual Basic)](../Topic/Extension%20Methods%20\(Visual%20Basic\).md).  
  
 For example, the following code example shows a custom aggregate function that calculates the median value of a collection of numbers. There are two overloads of the `Median` extension method. The first overload accepts, as input, a collection of type `IEnumerable(Of Double)`. If the `Median` aggregate function is called for a query field of type `Double`, this method will be called. The second overload of the `Median` method can be passed any generic type. The generic overload of the `Median` method takes a second parameter that references the `Func(Of T, Double)` lambda expression to project a value for a type (from a collection) as the corresponding value of type `Double`. It then delegates the calculation of the median value to the other overload of the `Median` method. For more information about lambda expressions, see [Lambda Expressions](../vs140/Lambda-Expressions--Visual-Basic-.md).  
  
 [!CODE [VbSimpleQuerySamples#18](../CodeSnippet/VS_Snippets_VBCSharp/VbSimpleQuerySamples#18)]  
  
 The following code example shows sample queries that call the `Median` aggregate function on a collection of type `Integer`, and a collection of type `Double`. The query that calls the `Median` aggregate function on the collection of type `Double` calls the overload of the `Median` method that accepts, as input, a collection of type `Double`. The query that calls the `Median` aggregate function on the collection of type `Integer` calls the generic overload of the `Median` method.  
  
 [!CODE [VbSimpleQuerySamples#19](../CodeSnippet/VS_Snippets_VBCSharp/VbSimpleQuerySamples#19)]  
  
## See Also  
 [Introduction to LINQ in Visual Basic](../Topic/Introduction%20to%20LINQ%20in%20Visual%20Basic.md)   
 [Queries (Visual Basic)](../vs140/Queries--Visual-Basic-.md)   
 [Select Clause](../Topic/Select%20Clause%20\(Visual%20Basic\).md)   
 [From Clause](../vs140/From-Clause--Visual-Basic-.md)   
 [Where Clause (Visual Basic)](../vs140/Where-Clause--Visual-Basic-.md)   
 [Group By Clause (Visual Basic)](../vs140/Group-By-Clause--Visual-Basic-.md)