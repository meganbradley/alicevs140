---
title: "Data Transformations with LINQ (C#)"
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
ms.assetid: 674eae9e-bc72-4a88-aed3-802b45b25811
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Data Transformations with LINQ (C#)
[!INCLUDE[vbteclinqext](../vs140/includes/vbteclinqext_md.md)] is not only about retrieving data. It is also a powerful tool for transforming data. By using a [!INCLUDE[vbteclinq](../vs140/includes/vbteclinq_md.md)] query, you can use a source sequence as input and modify it in many ways to create a new output sequence. You can modify the sequence itself without modifying the elements themselves by sorting and grouping. But perhaps the most powerful feature of [!INCLUDE[vbteclinq](../vs140/includes/vbteclinq_md.md)] queries is the ability to create new types. This is accomplished in the [select](../vs140/select-clause--C#-Reference-.md) clause. For example, you can perform the following tasks:  
  
-   Merge multiple input sequences into a single output sequence that has a new type.  
  
-   Create output sequences whose elements consist of only one or several properties of each element in the source sequence.  
  
-   Create output sequences whose elements consist of the results of operations performed on the source data.  
  
-   Create output sequences in a different format. For example, you can transform data from SQL rows or text files into XML.  
  
 These are just several examples. Of course, these transformations can be combined in various ways in the same query. Furthermore, the output sequence of one query can be used as the input sequence for a new query.  
  
## Joining Multiple Inputs into One Output Sequence  
 You can use a [!INCLUDE[vbteclinq](../vs140/includes/vbteclinq_md.md)] query to create an output sequence that contains elements from more than one input sequence. The following example shows how to combine two in-memory data structures, but the same principles can be applied to combine data from XML or SQL or DataSet sources. Assume the following two class types:  
  
 [!CODE [CsLINQGettingStarted#7](../CodeSnippet/VS_Snippets_VBCSharp/CsLINQGettingStarted#7)]  
  
 The following example shows the query:  
  
 [!CODE [CSLinqGettingStarted#8](../CodeSnippet/VS_Snippets_VBCSharp/CsLINQGettingStarted#8)]  
  
 For more information, see [join clause (C# Reference)](../Topic/join%20clause%20\(C%23%20Reference\).md) and [select clause (C# Reference)](../vs140/select-clause--C#-Reference-.md).  
  
## Selecting a Subset of each Source Element  
 There are two primary ways to select a subset of each element in the source sequence:  
  
1.  To select just one member of the source element, use the dot operation. In the following example, assume that a `Customer` object contains several public properties including a string named `City`. When executed, this query will produce an output sequence of strings.  
  
    ```  
    var query = from cust in Customers  
                select cust.City;  
    ```  
  
2.  To create elements that contain more than one property from the source element, you can use an object initializer with either a named object or an anonymous type. The following example shows the use of an anonymous type to encapsulate two properties from each `Customer` element:  
  
    ```  
    var query = from cust in Customer  
                select new {Name = cust.Name, City = cust.City};  
    ```  
  
 For more information, see [Object and Collection Initializers (C# Programming Guide)](../Topic/Object%20and%20Collection%20Initializers%20\(C%23%20Programming%20Guide\).md) and [Anonymous Types (C# Programming Guide)](../Topic/Anonymous%20Types%20\(C%23%20Programming%20Guide\).md).  
  
## Transforming in-Memory Objects into XML  
 [!INCLUDE[vbteclinq](../vs140/includes/vbteclinq_md.md)] queries make it easy to transform data between in-memory data structures, SQL databases, [!INCLUDE[vstecado](../vs140/includes/vstecado_md.md)] Datasets and XML streams or documents. The following example transforms objects in an in-memory data structure into XML elements.  
  
 [!CODE [CsLINQGettingStarted#9](../CodeSnippet/VS_Snippets_VBCSharp/CsLINQGettingStarted#9)]  
  
 The code produces the following XML output:  
  
```  
< Root>  
  <student>  
    <First>Svetlana</First>  
    <Last>Omelchenko</Last>  
    <Scores>97,92,81,60</Scores>  
  </student>  
  <student>  
    <First>Claire</First>  
    <Last>O'Donnell</Last>  
    <Scores>75,84,91,39</Scores>  
  </student>  
  <student>  
    <First>Sven</First>  
    <Last>Mortensen</Last>  
    <Scores>88,94,65,91</Scores>  
  </student>  
</Root>  
```  
  
 For more information, see [Creating XML Trees in C# (LINQ to XML)](../Topic/Creating%20XML%20Trees%20in%20C%23%20\(LINQ%20to%20XML\)2.md).  
  
## Performing Operations on Source Elements  
 An output sequence might not contain any elements or element properties from the source sequence. The output might instead be a sequence of values that is computed by using the source elements as input arguments. The following simple query, when it is executed, outputs a sequence of strings whose values represent a calculation based on the source sequence of elements of type `double`.  
  
> [!NOTE]
>  Calling methods in query expressions is not supported if the query will be translated into some other domain. For example, you cannot call an ordinary C# method in [!INCLUDE[vbtecdlinq](../vs140/includes/vbtecdlinq_md.md)] because SQL Server has no context for it. However, you can map stored procedures to methods and call those. For more information, see [Stored Procedures: Mapping and Calling (LINQ to SQL)](assetId:///4d23dd7a-a85f-44ff-a717-af7d0950c0fc).  
  
 [!CODE [CsLINQGettingStarted#10](../CodeSnippet/VS_Snippets_VBCSharp/CsLINQGettingStarted#10)]  
  
## See Also  
 [Language-Integrated Query (LINQ) (C#)](../Topic/Language-Integrated%20Query%20\(LINQ\)%20\(C%23\).md)   
 [LINQ to SQL](assetId:///73d13345-eece-471a-af40-4cc7a2f11655)   
 [LINQ to DataSet](assetId:///743e3755-3ecb-45a2-8d9b-9ed41f0dcf17)   
 [LINQ to XML (C#)](../Topic/LINQ%20to%20XML%20\(C%23\).md)   
 [LINQ Query Expressions (C# Programming Guide)](../Topic/LINQ%20Query%20Expressions%20\(C%23%20Programming%20Guide\).md)   
 [select clause (C# Reference)](../vs140/select-clause--C#-Reference-.md)