---
title: "Boolean Data Type (Visual Basic)"
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
ms.assetid: 4858e630-4813-4216-a55e-f4d0feb884e4
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Boolean Data Type (Visual Basic)
Holds values that can be only `True` or `False`. The keywords `True` and `False` correspond to the two states of `Boolean` variables.  
  
## Remarks  
 Use the [Boolean Data Type (Visual Basic)](../vs140/Boolean-Data-Type--Visual-Basic-.md) to contain two-state values such as true/false, yes/no, or on/off.  
  
 The default value of `Boolean` is `False`.  
  
 `Boolean` values are not stored as numbers, and the stored values are not intended to be equivalent to numbers. You should never write code that relies on equivalent numeric values for `True` and `False`. Whenever possible, you should restrict usage of `Boolean` variables to the logical values for which they are designed.  
  
## Type Conversions  
 When Visual Basic converts numeric data type values to `Boolean`, 0 becomes `False` and all other values become `True`. When Visual Basic converts `Boolean` values to numeric types, `False` becomes 0 and `True` becomes -1.  
  
 When you convert between `Boolean` values and numeric data types, keep in mind that the .NET Framework conversion methods do not always produce the same results as the Visual Basic conversion keywords. This is because the Visual Basic conversion retains behavior compatible with previous versions. For more information, see "Boolean Type Does Not Convert to Numeric Type Accurately" in [Troubleshooting Data Types](../Topic/Troubleshooting%20Data%20Types%20\(Visual%20Basic\).md).  
  
## Programming Tips  
  
-   **Negative Numbers.** `Boolean` is not a numeric type and cannot represent a negative value. In any case, you should not use `Boolean` to hold numeric values.  
  
-   **Type Characters.** `Boolean` has no literal type character or identifier type character.  
  
-   **Framework Type.** The corresponding type in the .NET Framework is the <xref:System.Boolean?qualifyHint=True> structure.  
  
## Example  
 In the following example, `runningVB` is a `Boolean` variable, which stores a simple yes/no setting.  
  
```  
Dim runningVB As Boolean  
' Check to see if program is running on Visual Basic engine.  
If scriptEngine = "VB" Then  
    runningVB = True  
End If  
```  
  
## See Also  
 <xref:System.Boolean?qualifyHint=True>   
 [Data Types](../Topic/Data%20Type%20Summary%20\(Visual%20Basic\).md)   
 [Type Conversion Functions](../vs140/Type-Conversion-Functions--Visual-Basic-.md)   
 [Conversion Summary](../vs140/Conversion-Summary--Visual-Basic-.md)   
 [Efficient Use of Data Types](../Topic/Efficient%20Use%20of%20Data%20Types%20\(Visual%20Basic\).md)   
 [Troubleshooting Data Types](../Topic/Troubleshooting%20Data%20Types%20\(Visual%20Basic\).md)   
 [CType Function](../Topic/CType%20Function%20\(Visual%20Basic\).md)