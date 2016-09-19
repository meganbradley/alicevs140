---
title: "How to: Declare a Property with Mixed Access Levels (Visual Basic)"
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
ms.assetid: fdbb2d97-279a-4956-b26c-cbdfbc34915a
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Declare a Property with Mixed Access Levels (Visual Basic)
If you want the `Get` and `Set` procedures on a property to have different access levels, you can use the more permissive level in the `Property` statement and the more restrictive level in either the `Get` or `Set` statement. You use mixed access levels on a property when you want certain parts of the code to be able to get the property's value, and certain other parts of the code to be able to change the value.  
  
 For more information on access levels, see [Access Levels in Visual Basic](../vs140/Access-Levels-in-Visual-Basic.md).  
  
### To declare a property with mixed access levels  
  
1.  Declare the property in the normal way, and specify the less restrictive access level (such as `Public`) in the `Property` statement.  
  
2.  Declare either the `Get` or the `Set` procedure specifying the more restrictive access level (such as `Friend`).  
  
3.  Do not specify an access level on the other property procedure. It assumes the access level declared in the `Property` statement. You can restrict access on only one of the property procedures.  
  
     [!CODE [VbVbcnProcedures#10](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnProcedures#10)]  
  
     In the preceding example, the `Get` procedure has the same `Protected` access as the property itself, while the `Set` procedure has `Private` access. A class derived from `employee` can read the `salary` value, but only the `employee` class can set it.  
  
## See Also  
 [Procedures in Visual Basic](../vs140/Procedures-in-Visual-Basic.md)   
 [Property Procedures](../vs140/Property-Procedures--Visual-Basic-.md)   
 [Procedure Parameters and Arguments](../vs140/Procedure-Parameters-and-Arguments--Visual-Basic-.md)   
 [Property Statement](../vs140/Property-Statement.md)   
 [Differences Between Properties and Variables in Visual Basic](../vs140/Differences-Between-Properties-and-Variables-in-Visual-Basic.md)   
 [How to: Create a Property](../vs140/How-to--Create-a-Property--Visual-Basic-.md)   
 [How to: Call a Property Procedure](../vs140/How-to--Call-a-Property-Procedure--Visual-Basic-.md)   
 [How to: Declare and Call a Default Property in Visual Basic](../Topic/How%20to:%20Declare%20and%20Call%20a%20Default%20Property%20in%20Visual%20Basic.md)   
 [How to: Put a Value in a Property](../Topic/How%20to:%20Put%20a%20Value%20in%20a%20Property%20\(Visual%20Basic\).md)   
 [How to: Get a Value from a Property](../vs140/How-to--Get-a-Value-from-a-Property--Visual-Basic-.md)