---
title: "How to: Use a Class that Defines Operators (Visual Basic)"
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
ms.assetid: 7ccce94a-6ca0-47d1-9f3f-13385d34f5d5
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Use a Class that Defines Operators (Visual Basic)
If you are using a class or structure that defines its own operators, you can access those operators from [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)].  
  
 Defining an operator on a class or structure is also called *overloading* the operator.  
  
## Example  
 The following example accesses the SQL structure <xref:System.Data.SqlTypes.SqlString?qualifyHint=False>, which defines the conversion operators ([CType Function](../Topic/CType%20Function%20\(Visual%20Basic\).md)) in both directions between a SQL string and a [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] string. Use `CType(`*SQL string expression*, `String)` to convert a SQL string to a [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] string, and `CType(`*Visual Basic string expression*, <xref:System.Data.SqlTypes.SqlString?qualifyHint=False>`)` to convert in the other direction.  
  
 [!CODE [VbVbcnProcedures#30](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnProcedures#30)]  
  
 [!CODE [VbVbcnProcedures#31](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnProcedures#31)]  
  
 The <xref:System.Data.SqlTypes.SqlString?qualifyHint=False> structure defines a conversion operator ([CType Function](../Topic/CType%20Function%20\(Visual%20Basic\).md)) from `String` to <xref:System.Data.SqlTypes.SqlString?qualifyHint=False> and another from <xref:System.Data.SqlTypes.SqlString?qualifyHint=False> to `String`. The statement that assigns `title` to `jobTitle` makes use of the first operator, and the <xref:Microsoft.VisualBasic.Interaction.MsgBox?qualifyHint=False> function call uses the second.  
  
## Compiling the Code  
 Be sure the class or structure you are using defines the operator you want to use. Do not assume that the class or structure has defined every operator available for overloading. For a list of available operators, see [Operator Statement](../vs140/Operator-Statement.md).  
  
 Include the appropriate `Imports` statement for the SQL string at the beginning of your source file (in this case <xref:System.Data.SqlTypes?qualifyHint=False>).  
  
 Your project must have references to System.Data and System.XML.  
  
## See Also  
 [Operator Procedures](../vs140/Operator-Procedures--Visual-Basic-.md)   
 [How to: Define an Operator](../vs140/How-to--Define-an-Operator--Visual-Basic-.md)   
 [How to: Define a Conversion Operator](../vs140/How-to--Define-a-Conversion-Operator--Visual-Basic-.md)   
 [How to: Call an Operator Procedure](../Topic/How%20to:%20Call%20an%20Operator%20Procedure%20\(Visual%20Basic\).md)   
 [Widening](../vs140/Widening--Visual-Basic-.md)   
 [Narrowing](../vs140/Narrowing--Visual-Basic-.md)   
 [Structure Statement](../Topic/Structure%20Statement.md)   
 [How to: Declare a Structure](../vs140/How-to--Declare-a-Structure--Visual-Basic-.md)   
 [Implicit and Explicit Conversions](../Topic/Implicit%20and%20Explicit%20Conversions%20\(Visual%20Basic\).md)   
 [Widening and Narrowing Conversions](../Topic/Widening%20and%20Narrowing%20Conversions%20\(Visual%20Basic\).md)