---
title: "Matching &#39;&lt;operatorsymbol1&gt;&#39; operator is required for &#39;&lt;operatorsymbol2&gt;&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d2805e4f-08a8-4760-9539-565f51b88d13
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Matching &#39;&lt;operatorsymbol1&gt;&#39; operator is required for &#39;&lt;operatorsymbol2&gt;&#39;
An operator is defined when its required matching operator is not defined.  
  
 The following operators must be defined as matched pairs:  
  
-   `=` and `<>`  
  
-   `>` and `<`  
  
-   `>=` and `<=`  
  
-   `IsTrue` and `IsFalse`  
  
 If you define any of these operators in a class or structure, you must also define its matching operator in the same class or structure.  
  
 Even if you do not use the matching operator explicitly, [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] might need to use it. For example, if you define a class or structure that you use as the counter variable in a [For...Next Statement (Visual Basic)](../Topic/For...Next%20Statement%20\(Visual%20Basic\).md), [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] requires both the `>=` and `<=` operators (as well as the `+` operator).  
  
 **Error ID:** BC33033  
  
### To correct this error  
  
-   Define the matching operator in the same class or structure. Make every effort to define it meaningfully, because [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] might use it in a situation you do not anticipate.  
  
## See Also  
 [Operator Procedures](../vs140/Operator-Procedures--Visual-Basic-.md)   
 [Operator Statement](../vs140/Operator-Statement.md)   
 [How to: Define an Operator](../vs140/How-to--Define-an-Operator--Visual-Basic-.md)   
 [How to: Define a Conversion Operator](../vs140/How-to--Define-a-Conversion-Operator--Visual-Basic-.md)   
 [Operators and Expressions in Visual Basic](../vs140/Operators-and-Expressions-in-Visual-Basic.md)