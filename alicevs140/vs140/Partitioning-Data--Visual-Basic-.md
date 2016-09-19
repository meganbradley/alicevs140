---
title: "Partitioning Data (Visual Basic)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-visual-basic
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 69c59379-b66e-422c-b324-5b5c07760ef7
caps.latest.revision: 5
---
# Partitioning Data (Visual Basic)
Partitioning in LINQ refers to the operation of dividing an input sequence into two sections, without rearranging the elements, and then returning one of the sections.  
  
 The following illustration shows the results of three different partitioning operations on a sequence of characters. The first operation returns the first three elements in the sequence. The second operation skips the first three elements and returns the remaining elements. The third operation skips the first two elements in the sequence and returns the next three elements.  
  
 ![LINQ Partitioning Operations](../vs140/media/LINQ_Partition.png "LINQ_Partition")  
  
 The standard query operator methods that partition sequences are listed in the following section.  
  
## Operators  
  
|Operator Name|Description|Visual Basic Query Expression Syntax|More Information|  
|-------------------|-----------------|------------------------------------------|----------------------|  
|Skip|Skips elements up to a specified position in a sequence.|`Skip`|<xref:System.Linq.Enumerable.Skip``1?qualifyHint=True><br /><br /> <xref:System.Linq.Queryable.Skip``1?qualifyHint=True>|  
|SkipWhile|Skips elements based on a predicate function until an element does not satisfy the condition.|`Skip While`|<xref:System.Linq.Enumerable.SkipWhile?qualifyHint=True><br /><br /> <xref:System.Linq.Queryable.SkipWhile``1?qualifyHint=True>|  
|Take|Takes elements up to a specified position in a sequence.|`Take`|<xref:System.Linq.Enumerable.Take``1?qualifyHint=True><br /><br /> <xref:System.Linq.Queryable.Take``1?qualifyHint=True>|  
|TakeWhile|Takes elements based on a predicate function until an element does not satisfy the condition.|`Take While`|<xref:System.Linq.Enumerable.TakeWhile?qualifyHint=True><br /><br /> <xref:System.Linq.Queryable.TakeWhile``1?qualifyHint=True>|  
  
## Query Expression Syntax Examples  
  
### Skip  
 The following code example uses the `Skip` clause in [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] to skip over the first four strings in an array of strings before returning the remaining strings in the array.  
  
 [!CODE [CsLINQPartitioning#1](../CodeSnippet/VS_Snippets_VBCSharp/CsLINQPartitioning#1)]  
  
### SkipWhile  
 The following code example uses the `Skip While` clause in [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] to skip over the strings in an array while the first letter of the string is "a". The remaining strings in the array are returned.  
  
 [!CODE [CsLINQPartitioning#2](../CodeSnippet/VS_Snippets_VBCSharp/CsLINQPartitioning#2)]  
  
### Take  
 The following code example uses the `Take` clause in [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] to return the first two strings in an array of strings.  
  
 [!CODE [CsLINQPartitioning#3](../CodeSnippet/VS_Snippets_VBCSharp/CsLINQPartitioning#3)]  
  
### TakeWhile  
 The following code example uses the `Take While` clause in [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] to return strings from an array while the length of the string is five or less.  
  
 [!CODE [CsLINQPartitioning#4](../CodeSnippet/VS_Snippets_VBCSharp/CsLINQPartitioning#4)]  
  
## See Also  
 <xref:System.Linq?qualifyHint=False>   
 [Standard Query Operators Overview (Visual Basic)](../Topic/Standard%20Query%20Operators%20Overview%20\(Visual%20Basic\).md)   
 [Skip Clause (Visual Basic)](../vs140/Skip-Clause--Visual-Basic-.md)   
 [Skip While Clause (Visual Basic)](../vs140/Skip-While-Clause--Visual-Basic-.md)   
 [Take Clause (Visual Basic)](../vs140/Take-Clause--Visual-Basic-.md)   
 [Take While Clause (Visual Basic)](../vs140/Take-While-Clause--Visual-Basic-.md)