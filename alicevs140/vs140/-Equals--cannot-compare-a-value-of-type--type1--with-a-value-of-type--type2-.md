---
title: "&#39;Equals&#39; cannot compare a value of type &lt;type1&gt; with a value of type &lt;type2&gt;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: bd40bf57-3a12-407a-8622-7e428850c77c
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;Equals&#39; cannot compare a value of type &lt;type1&gt; with a value of type &lt;type2&gt;
An `Equals` operator in a `Join` or `Group Join` clause has attempted to compare one data type to another in a way that is not defined. An example of this is a comparison of a `Boolean` value to a `Date` type.  
  
 **Error ID:** BC36621  
  
### To correct this error  
  
-   Make sure that the values on each side of the `Equals` operator can be converted to a common data type. Some options for accomplishing this are:  
  
    -   Use the `CType` function to convert one or more of the values to a specific type.  
  
    -   Use the <xref:System.Convert?qualifyHint=False> class or conversion methods to convert one or more of the values to a common, immutable type.  
  
    -   Convert the values to strings by using the `ToString` method.  
  
## See Also  
 [CType Function](../Topic/CType%20Function%20\(Visual%20Basic\).md)   
 [Type Conversions in Visual Basic](../vs140/Type-Conversions-in-Visual-Basic.md)   
 [Join Clause (Visual Basic)](../vs140/Join-Clause--Visual-Basic-.md)   
 [Group Join Clause (Visual Basic)](../vs140/Group-Join-Clause--Visual-Basic-.md)   
 [Introduction to LINQ in Visual Basic](../Topic/Introduction%20to%20LINQ%20in%20Visual%20Basic.md)   
 [LINQ in Visual Basic](../vs140/LINQ-in-Visual-Basic.md)