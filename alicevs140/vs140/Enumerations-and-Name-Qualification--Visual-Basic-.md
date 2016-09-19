---
title: "Enumerations and Name Qualification (Visual Basic)"
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
ms.assetid: 08ba2738-df52-4140-bc55-f57c871c9b73
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Enumerations and Name Qualification (Visual Basic)
Normally, when referring to a member of an enumeration, you must qualify the member name with the enumeration name. For example, to refer to the `Sunday` member of your `Days` enumeration, you would use the following syntax:  
  
 [!CODE [VbEnumsTask#18](../CodeSnippet/VS_Snippets_VBCSharp/VbEnumsTask#18)]  
  
## Using the Imports Statement  
 You can avoid using fully qualified names by adding an `Imports` statement to the namespace declarations section of your code, as in the following example:  
  
 [!CODE [VbEnumsTask#22](../CodeSnippet/VS_Snippets_VBCSharp/VbEnumsTask#22)]  
  
 An `Imports` statement imports namespace names from referenced projects and assemblies and from within the same project as the module in which the statement appears. Once this statement is added, you can refer to your enumeration members without qualification, as in the following example:  
  
 [!CODE [VbEnumsTask#24](../CodeSnippet/VS_Snippets_VBCSharp/VbEnumsTask#24)]  
  
 By organizing sets of related constants in enumerations, you can use the same constant names in different contexts. For example, you can use the same names for the weekday constants in the `Days` and `WorkDays` enumerations. If you use the `Imports` statement with your enumerations, you must be careful to avoid ambiguous references. Consider the following example:  
  
 [!CODE [VbEnumsTask#22](../CodeSnippet/VS_Snippets_VBCSharp/VbEnumsTask#22)]  
  
 [!CODE [VbEnumsTask#25](../CodeSnippet/VS_Snippets_VBCSharp/VbEnumsTask#25)]  
  
 Assuming that `Monday` is a member of both the `Days` enumeration and the `Workdays` enumeration, this code generates a compiler error. To avoid ambiguous references when referring to an individual constant, qualify the constant name with its enumeration. The following code refers to the `Saturday` constants in the `Days` and `WorkDays` enumerations.  
  
 [!CODE [VbEnumsTask#32](../CodeSnippet/VS_Snippets_VBCSharp/VbEnumsTask#32)]  
  
## See Also  
 [Constants and Enumerations (Visual Basic)](../Topic/Constants%20and%20Enumerations%20\(Visual%20Basic\).md)   
 [How to: Declare an Enumeration](../vs140/How-to--Declare-Enumerations--Visual-Basic-.md)   
 [How to: Refer to an Enumeration Member](../vs140/How-to--Refer-to-an-Enumeration-Member--Visual-Basic-.md)   
 [How to: Iterate Through An Enumeration in Visual Basic](../Topic/How%20to:%20Iterate%20Through%20An%20Enumeration%20in%20Visual%20Basic.md)   
 [How to: Determine the String Associated with an Enumeration Value](../Topic/How%20to:%20Determine%20the%20String%20Associated%20with%20an%20Enumeration%20Value%20\(Visual%20Basic\).md)   
 [When to Use an Enumeration](../vs140/When-to-Use-an-Enumeration--Visual-Basic-.md)   
 [Constant and Literal Data Types](../vs140/Constant-and-Literal-Data-Types--Visual-Basic-.md)   
 [Enum Statement](../Topic/Enum%20Statement%20\(Visual%20Basic\).md)   
 [Imports Statement (.NET Namespace and Type)](../Topic/Imports%20Statement%20\(.NET%20Namespace%20and%20Type\).md)   
 [Data Type Summary (Visual Basic)](../Topic/Data%20Type%20Summary%20\(Visual%20Basic\).md)