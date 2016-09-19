---
title: "Overload Resolution (Visual Basic)"
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
ms.assetid: 766115d1-4352-45fb-859f-6063e0de0ec0
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Overload Resolution (Visual Basic)
When the [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] compiler encounters a call to a procedure that is defined in several overloaded versions, the compiler must decide which of the overloads to call. It does this by performing the following steps:  
  
1.  **Accessibility.** It eliminates any overload with an access level that prevents the calling code from calling it.  
  
2.  **Number of Parameters.** It eliminates any overload that defines a different number of parameters than are supplied in the call.  
  
3.  **Parameter Data Types.** The compiler gives instance methods preference over extension methods. If any instance method is found that requires only widening conversions to match the procedure call, all extension methods are dropped and the compiler continues with only the instance method candidates. If no such instance method is found, it continues with both instance and extension methods.  
  
     In this step, it eliminates any overload for which the data types of the calling arguments cannot be converted to the parameter types defined in the overload.  
  
4.  **Narrowing Conversions.** It eliminates any overload that requires a narrowing conversion from the calling argument types to the defined parameter types. This is true whether the type checking switch ([Option Strict Statement](../vs140/Option-Strict-Statement.md)) is `On` or `Off`.  
  
5.  **Least Widening.** The compiler considers the remaining overloads in pairs. For each pair, it compares the data types of the defined parameters. If the types in one of the overloads all widen to the corresponding types in the other, the compiler eliminates the latter. That is, it retains the overload that requires the least amount of widening.  
  
6.  **Single Candidate.** It continues considering overloads in pairs until only one overload remains, and it resolves the call to that overload. If the compiler cannot reduce the overloads to a single candidate, it generates an error.  
  
 The following illustration shows the process that determines which of a set of overloaded versions to call.  
  
 ![Flow diagram of overload resolution process](../vs140/media/OverloadRes.gif "OverloadRes")  
Resolving among overloaded versions  
  
 The following example illustrates this overload resolution process.  
  
 [!CODE [VbVbcnProcedures#62](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnProcedures#62)]  
  
 [!CODE [VbVbcnProcedures#63](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnProcedures#63)]  
  
 In the first call, the compiler eliminates the first overload because the type of the first argument (`Short`) narrows to the type of the corresponding parameter (`Byte`). It then eliminates the third overload because each argument type in the second overload (`Short` and `Single`) widens to the corresponding type in the third overload (`Integer` and `Single`). The second overload requires less widening, so the compiler uses it for the call.  
  
 In the second call, the compiler cannot eliminate any of the overloads on the basis of narrowing. It eliminates the third overload for the same reason as in the first call, because it can call the second overload with less widening of the argument types. However, the compiler cannot resolve between the first and second overloads. Each has one defined parameter type that widens to the corresponding type in the other (`Byte` to `Short`, but `Single` to `Double`). The compiler therefore generates an overload resolution error.  
  
## Overloaded Optional and ParamArray Arguments  
 If two overloads of a procedure have identical signatures except that the last parameter is declared [Optional (Visual Basic)](../vs140/Optional--Visual-Basic-.md) in one and [ParamArray](../vs140/ParamArray--Visual-Basic-.md) in the other, the compiler resolves a call to that procedure as follows:  
  
|||  
|-|-|  
|If the call supplies the last argument as|The compiler resolves the call to the overload declaring the last argument as|  
|No value (argument omitted)|`Optional`|  
|A single value|`Optional`|  
|Two or more values in a comma-separated list|`ParamArray`|  
|An array of any length (including an empty array)|`ParamArray`|  
  
## See Also  
 [Optional Parameters](../vs140/Optional-Parameters--Visual-Basic-.md)   
 [Parameter Arrays](../Topic/Parameter%20Arrays%20\(Visual%20Basic\).md)   
 [Procedure Overloading](../Topic/Procedure%20Overloading%20\(Visual%20Basic\).md)   
 [Troubleshooting Procedures](../vs140/Troubleshooting-Procedures--Visual-Basic-.md)   
 [How to: Define Multiple Versions of a Procedure](../vs140/How-to--Define-Multiple-Versions-of-a-Procedure--Visual-Basic-.md)   
 [How to: Call an Overloaded Procedure](../vs140/How-to--Call-an-Overloaded-Procedure--Visual-Basic-.md)   
 [How to: Overload a Procedure that Takes Optional Parameters](../vs140/How-to--Overload-a-Procedure-that-Takes-Optional-Parameters--Visual-Basic-.md)   
 [How to: Overload a Procedure that Takes an Indefinite Number of Parameters](../vs140/How-to--Overload-a-Procedure-that-Takes-an-Indefinite-Number-of-Parameters--Visual-Basic-.md)   
 [Considerations in Overloading Procedures](../vs140/Considerations-in-Overloading-Procedures--Visual-Basic-.md)   
 [Overloads](../vs140/Overloads--Visual-Basic-.md)   
 [Extension Methods](../Topic/Extension%20Methods%20\(Visual%20Basic\).md)