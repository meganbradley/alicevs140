---
title: "Data Types in Visual Basic"
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
ms.assetid: 5e1b9aaf-c7ca-4b29-9b22-0e82ed8e85e2
caps.latest.revision: 30
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Data Types in Visual Basic
The *data type* of a programming element refers to what kind of data it can hold and how it stores that data. Data types apply to all values that can be stored in computer memory or participate in the evaluation of an expression. Every variable, literal, constant, enumeration, property, procedure parameter, procedure argument, and procedure return value has a data type.  
  
## Declared Data Types  
 You define a programming element with a declaration statement, and you specify its data type with the `As` clause. The following table shows the statements you use to declare various elements.  
  
|Programming element|Data type declaration|  
|-------------------------|---------------------------|  
|Variable|In a [Dim Statement (Visual Basic)](../Topic/Dim%20Statement%20\(Visual%20Basic\).md)<br /><br /> `Dim`   `amount As Double`<br /><br /> `Static`   `yourName As String`<br /><br /> `Public`   `billsPaid As Decimal = 0`|  
|Literal|With a literal type character; see "Literal Type Characters" in [Type Characters](../vs140/Type-Characters--Visual-Basic-.md)<br /><br /> `Dim searchChar As Char = "."`  `C`|  
|Constant|In a [Const Statement (Visual Basic)](../Topic/Const%20Statement%20\(Visual%20Basic\).md)<br /><br /> `Const`   `modulus As Single = 4.17825F`|  
|Enumeration|In an [Enum Statement (Visual Basic)](../Topic/Enum%20Statement%20\(Visual%20Basic\).md)<br /><br /> `Public`   `Enum`   `colors`|  
|Property|In a [Property Statement](../vs140/Property-Statement.md)<br /><br /> `Property`   `region() As String`|  
|Procedure parameter|In a [Sub Statement (Visual Basic)](../Topic/Sub%20Statement%20\(Visual%20Basic\).md), [Function Statement (Visual Basic)](../Topic/Function%20Statement%20\(Visual%20Basic\).md), or [Operator Statement](../vs140/Operator-Statement.md)<br /><br /> `Sub addSale(ByVal`   `amount`   `As Double)`|  
|Procedure argument|In the calling code; each argument is a programming element that has already been declared, or an expression containing declared elements<br /><br /> `subString = Left(`  `inputString`  `,`   `5`  `)`|  
|Procedure return value|In a [Function Statement (Visual Basic)](../Topic/Function%20Statement%20\(Visual%20Basic\).md) or [Operator Statement](../vs140/Operator-Statement.md)<br /><br /> `Function convert(ByVal b As Byte)`   `As String`|  
  
 For a list of Visual Basic data types, see [Data Type Summary (Visual Basic)](../Topic/Data%20Type%20Summary%20\(Visual%20Basic\).md).  
  
## See Also  
 [Type Characters](../vs140/Type-Characters--Visual-Basic-.md)   
 [Elementary Data Types](../vs140/Elementary-Data-Types--Visual-Basic-.md)   
 [Composite Data Types](../vs140/Composite-Data-Types--Visual-Basic-.md)   
 [Generic Types in Visual Basic](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)   
 [Value Types and Reference Types](../Topic/Value%20Types%20and%20Reference%20Types.md)   
 [Type Conversions in Visual Basic](../vs140/Type-Conversions-in-Visual-Basic.md)   
 [Structures](../vs140/Structures--Visual-Basic-.md)   
 [Troubleshooting Data Types](../Topic/Troubleshooting%20Data%20Types%20\(Visual%20Basic\).md)   
 [Data Types](../Topic/Data%20Type%20Summary%20\(Visual%20Basic\).md)   
 [Efficient Use of Data Types (Visual Basic)](../Topic/Efficient%20Use%20of%20Data%20Types%20\(Visual%20Basic\).md)