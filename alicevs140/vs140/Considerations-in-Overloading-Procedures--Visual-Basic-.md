---
title: "Considerations in Overloading Procedures (Visual Basic)"
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
ms.assetid: a2001248-10d0-42c5-b0ce-eeedc987319f
caps.latest.revision: 28
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Considerations in Overloading Procedures (Visual Basic)
When you overload a procedure, you must use a different *signature* for each overloaded version. This usually means each version must specify a different parameter list. For more information, see "Different Signature" in [Procedure Overloading](../Topic/Procedure%20Overloading%20\(Visual%20Basic\).md).  
  
 You can overload a `Function` procedure with a `Sub` procedure, and vice versa, provided they have different signatures. Two overloads cannot differ only in that one has a return value and the other does not.  
  
 You can overload a property the same way you overload a procedure, and with the same restrictions. However, you cannot overload a procedure with a property, or vice versa.  
  
## Alternatives to Overloaded Versions  
 You sometimes have alternatives to overloaded versions, particularly when the presence of arguments is optional or their number is variable.  
  
 Keep in mind that optional arguments are not necessarily supported by all languages, and parameter arrays are limited to [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)]. If you are writing a procedure that is likely to be called from code written in any of several different languages, overloaded versions offer the greatest flexibility.  
  
### Overloads and Optional Arguments  
 When the calling code can optionally supply or omit one or more arguments, you can define multiple overloaded versions or use optional parameters.  
  
#### When to Use Overloaded Versions  
 You can consider defining a series of overloaded versions in the following cases:  
  
-   The logic in the procedure code is significantly different depending on whether the calling code supplies an optional argument or not.  
  
-   The procedure code cannot reliably test whether the calling code has supplied an optional argument. This is the case, for example, if there is no possible candidate for a default value that the calling code could not be expected to supply.  
  
#### When to Use Optional Parameters  
 You might prefer one or more optional parameters in the following cases:  
  
-   The only required action when the calling code does not supply an optional argument is to set the parameter to a default value. In such a case, the procedure code can be less complicated if you define a single version with one or more `Optional` parameters.  
  
 For more information, see [Optional Parameters](../vs140/Optional-Parameters--Visual-Basic-.md).  
  
### Overloads and ParamArrays  
 When the calling code can pass a variable number of arguments, you can define multiple overloaded versions or use a parameter array.  
  
#### When to Use Overloaded Versions  
 You can consider defining a series of overloaded versions in the following cases:  
  
-   You know that the calling code never passes more than a small number of values to the parameter array.  
  
-   The logic in the procedure code is significantly different depending on how many values the calling code passes.  
  
-   The calling code can pass values of different data types.  
  
#### When to Use a Parameter Array  
 You are better served by a `ParamArray` parameter in the following cases:  
  
-   You are not able to predict how many values the calling code can pass to the parameter array, and it could be a large number.  
  
-   The procedure logic lends itself to iterating through all the values the calling code passes, performing essentially the same operations on every value.  
  
 For more information, see [Parameter Arrays](../Topic/Parameter%20Arrays%20\(Visual%20Basic\).md).  
  
## Implicit Overloads for Optional Parameters  
 A procedure with an [Optional (Visual Basic)](../vs140/Optional--Visual-Basic-.md) parameter is equivalent to two overloaded procedures, one with the optional parameter and one without it. You cannot overload such a procedure with a parameter list corresponding to either of these. The following declarations illustrate this.  
  
 [!CODE [VbVbcnProcedures#58](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnProcedures#58)]  
  
 [!CODE [VbVbcnProcedures#60](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnProcedures#60)]  
  
 [!CODE [VbVbcnProcedures#61](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnProcedures#61)]  
  
 For a procedure with more than one optional parameter, there is a set of implicit overloads, arrived at by logic similar to that in the preceding example.  
  
## Implicit Overloads for a ParamArray Parameter  
 The compiler considers a procedure with a [ParamArray](../vs140/ParamArray--Visual-Basic-.md) parameter to have an infinite number of overloads, differing from each other in what the calling code passes to the parameter array, as follows:  
  
-   One overload for when the calling code does not supply an argument to the `ParamArray`  
  
-   One overload for when the calling code supplies a one-dimensional array of the `ParamArray` element type  
  
-   For every positive integer, one overload for when the calling code supplies that number of arguments, each of the `ParamArray` element type  
  
 The following declarations illustrate these implicit overloads.  
  
 [!CODE [VbVbcnProcedures#68](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnProcedures#68)]  
  
 [!CODE [VbVbcnProcedures#70](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnProcedures#70)]  
  
 You cannot overload such a procedure with a parameter list that takes a one-dimensional array for the parameter array. However, you can use the signatures of the other implicit overloads. The following declarations illustrate this.  
  
 [!CODE [VbVbcnProcedures#71](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnProcedures#71)]  
  
## Typeless Programming as an Alternative to Overloading  
 If you want to allow the calling code to pass different data types to a parameter, an alternative approach is typeless programming. You can set the type checking switch to `Off` with either the [Option Strict Statement](../vs140/Option-Strict-Statement.md) or the [/optionstrict](../vs140/-optionstrict.md) compiler option. Then you do not have to declare the parameter's data type. However, this approach has the following disadvantages compared to overloading:  
  
-   Typeless programming produces less efficient execution code.  
  
-   The procedure must test for every data type it anticipates being passed.  
  
-   The compiler cannot signal an error if the calling code passes a data type that the procedure does not support.  
  
## See Also  
 [Procedures in Visual Basic](../vs140/Procedures-in-Visual-Basic.md)   
 [Procedure Parameters and Arguments](../vs140/Procedure-Parameters-and-Arguments--Visual-Basic-.md)   
 [Troubleshooting Procedures](../vs140/Troubleshooting-Procedures--Visual-Basic-.md)   
 [How to: Define Multiple Versions of a Procedure](../vs140/How-to--Define-Multiple-Versions-of-a-Procedure--Visual-Basic-.md)   
 [How to: Call an Overloaded Procedure](../vs140/How-to--Call-an-Overloaded-Procedure--Visual-Basic-.md)   
 [How to: Overload a Procedure that Takes Optional Parameters](../vs140/How-to--Overload-a-Procedure-that-Takes-Optional-Parameters--Visual-Basic-.md)   
 [How to: Overload a Procedure that Takes an Indefinite Number of Parameters](../vs140/How-to--Overload-a-Procedure-that-Takes-an-Indefinite-Number-of-Parameters--Visual-Basic-.md)   
 [Overload Resolution](../vs140/Overload-Resolution--Visual-Basic-.md)   
 [Overloads](../vs140/Overloads--Visual-Basic-.md)