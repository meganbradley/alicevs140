---
title: "How to: Overload a Procedure that Takes Optional Parameters (Visual Basic)"
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
ms.assetid: 825f9d56-4cde-43fd-993a-b9171717e2eb
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Overload a Procedure that Takes Optional Parameters (Visual Basic)
If a procedure has one or more [Optional (Visual Basic)](../vs140/Optional--Visual-Basic-.md) parameters, you cannot define an overloaded version matching any of its implicit overloads. For more information, see "Implicit Overloads for Optional Parameters" in [Considerations in Overloading Procedures](../vs140/Considerations-in-Overloading-Procedures--Visual-Basic-.md).  
  
## One Optional Parameter  
  
#### To overload a procedure that takes one optional parameter  
  
1.  Write a `Sub` or `Function` declaration statement that includes the optional parameter in the parameter list. Do not use the `Optional` keyword in this overloaded version.  
  
2.  Precede the `Sub` or `Function` keyword with the [Overloads](../vs140/Overloads--Visual-Basic-.md) keyword.  
  
3.  Write the procedure code that should execute when the calling code supplies the optional argument.  
  
4.  Terminate the procedure with the `End Sub` or `End Function` statement as appropriate.  
  
5.  Write a second declaration statement that is identical to the first declaration except that it does not include the optional parameter in the parameter list.  
  
6.  Write the procedure code that should execute when the calling code does not supply the optional argument. Terminate the procedure with the `End Sub` or `End Function` statement as appropriate.  
  
     The following example shows a procedure defined with an optional parameter,  an equivalent set of two overloaded procedures, and finally examples of both invalid and valid overloaded versions.  
  
     [!CODE [VbVbcnProcedures#59](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnProcedures#59)]  
  
     [!CODE [VbVbcnProcedures#60](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnProcedures#60)]  
  
     [!CODE [VbVbcnProcedures#61](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnProcedures#61)]  
  
## Multiple Optional Parameters  
 For a procedure with more than one optional parameter, you normally need more than two overloaded versions. For example, if there are two optional parameters, and the calling code can supply or omit each one independently of the other, you need four overloaded versions, one for each possible combination of supplied arguments.  
  
 As the number of optional parameters increases, the complexity of the overloading increases. Unless some combinations of supplied arguments are not acceptable, for N optional parameters you need 2 ^ N overloaded versions. Depending on the nature of the procedure, you might find that the clarity of logic justifies the extra effort of defining all the overloaded versions.  
  
#### To overload a procedure that takes more than one optional parameter  
  
1.  Determine which combinations of supplied optional arguments are acceptable to the logic of the procedure. An unacceptable combination might arise if one optional parameter depends on another. For example, if one parameter accepts a spouse's name and another accepts the spouse's age, a combination of arguments supplying the age but omitting the name is unacceptable.  
  
2.  For each acceptable combination of supplied optional arguments, write a `Sub` or `Function` declaration statement that defines the corresponding parameter list. Do not use the `Optional` keyword.  
  
3.  In each declaration, precede the `Sub` or `Function` keyword with the [Overloads](../vs140/Overloads--Visual-Basic-.md) keyword.  
  
4.  Following each declaration, write the procedure code that should execute when the calling code supplies an argument list corresponding to that declaration's parameter list.  
  
5.  Terminate each procedure with the `End Sub` or `End Function` statement as appropriate.  
  
## See Also  
 [Procedures in Visual Basic](../vs140/Procedures-in-Visual-Basic.md)   
 [Procedure Parameters and Arguments](../vs140/Procedure-Parameters-and-Arguments--Visual-Basic-.md)   
 [Optional Parameters](../vs140/Optional-Parameters--Visual-Basic-.md)   
 [Parameter Arrays](../Topic/Parameter%20Arrays%20\(Visual%20Basic\).md)   
 [Procedure Overloading](../Topic/Procedure%20Overloading%20\(Visual%20Basic\).md)   
 [Troubleshooting Procedures](../vs140/Troubleshooting-Procedures--Visual-Basic-.md)   
 [How to: Define Multiple Versions of a Procedure](../vs140/How-to--Define-Multiple-Versions-of-a-Procedure--Visual-Basic-.md)   
 [How to: Call an Overloaded Procedure](../vs140/How-to--Call-an-Overloaded-Procedure--Visual-Basic-.md)   
 [How to: Overload a Procedure that Takes an Indefinite Number of Parameters](../vs140/How-to--Overload-a-Procedure-that-Takes-an-Indefinite-Number-of-Parameters--Visual-Basic-.md)   
 [Overload Resolution](../vs140/Overload-Resolution--Visual-Basic-.md)