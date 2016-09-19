---
title: "How to: Define Multiple Versions of a Procedure (Visual Basic)"
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
ms.assetid: 71ccdd66-1b00-4b66-bee4-6926c0d696f4
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Define Multiple Versions of a Procedure (Visual Basic)
You can define a procedure in multiple versions by *overloading* it, using the same name but a different parameter list for each version. The purpose of overloading is to define several closely related versions of a procedure without having to differentiate them by name.  
  
 For more information, see [Procedure Overloading](../Topic/Procedure%20Overloading%20\(Visual%20Basic\).md).  
  
### To define multiple versions of a procedure  
  
1.  Write a `Sub` or `Function` declaration statement for each version of the procedure you want to define. Use the same procedure name in every declaration.  
  
2.  Precede the `Sub` or `Function` keyword in each declaration with the [Overloads](../vs140/Overloads--Visual-Basic-.md) keyword. You can optionally omit `Overloads` in the declarations, but if you include it in any of the declarations, you must include it in every declaration.  
  
3.  Following each declaration statement, write procedure code to handle the specific case where the calling code supplies arguments matching that version's parameter list. You do not have to test for which parameters the calling code has supplied. [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] passes control to the matching version of your procedure.  
  
4.  Terminate each version of the procedure with the `End Sub` or `End Function` statement as appropriate.  
  
## Example  
 The following example defines a `Sub` procedure to post a transaction against a customer's balance. It uses the `Overloads` keyword to define two versions of the procedure, one that accepts the customer by name and the other by account number.  
  
 [!CODE [VbVbcnProcedures#72](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnProcedures#72)]  
  
 The calling code can obtain the customer identification as either a `String` or an `Integer`, and then use the same calling statement in either case.  
  
 For information on how to call these versions of the `post` procedure, see [How to: Call an Overloaded Procedure](../vs140/How-to--Call-an-Overloaded-Procedure--Visual-Basic-.md).  
  
## Compiling the Code  
 Make sure each of your overloaded versions has the same procedure name but a different parameter list.  
  
## See Also  
 [Procedures in Visual Basic](../vs140/Procedures-in-Visual-Basic.md)   
 [Procedure Parameters and Arguments](../vs140/Procedure-Parameters-and-Arguments--Visual-Basic-.md)   
 [Troubleshooting Procedures](../vs140/Troubleshooting-Procedures--Visual-Basic-.md)   
 [How to: Overload a Procedure that Takes Optional Parameters](../vs140/How-to--Overload-a-Procedure-that-Takes-Optional-Parameters--Visual-Basic-.md)   
 [How to: Overload a Procedure that Takes an Indefinite Number of Parameters](../vs140/How-to--Overload-a-Procedure-that-Takes-an-Indefinite-Number-of-Parameters--Visual-Basic-.md)   
 [Considerations in Overloading Procedures](../vs140/Considerations-in-Overloading-Procedures--Visual-Basic-.md)   
 [Overload Resolution](../vs140/Overload-Resolution--Visual-Basic-.md)