---
title: "Declared Element Characteristics (Visual Basic)"
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
ms.assetid: 1bc40fb8-b67c-4428-90a4-76b630ae2583
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Declared Element Characteristics (Visual Basic)
A *characteristic* of a declared element is an aspect of that element that affects how code can interact with it. Every declared element has one or more of the following characteristics associated with it:  
  
-   *Data type* — the values the element can hold, and how it stores those values. For more information, see [Data Type Summary (Visual Basic)](../Topic/Data%20Type%20Summary%20\(Visual%20Basic\).md).  
  
-   *Lifetime* — the period of execution time during which the element is available for use. For more information, see [Lifetime in Visual Basic](../vs140/Lifetime-in-Visual-Basic.md).  
  
-   *Scope* — the set of all code that can refer to the element without qualifying its name. For more information, see [How to: Control the Scope of a Variable](../vs140/How-to--Control-the-Scope-of-a-Variable--Visual-Basic-.md).  
  
-   *Access level* — the permission for code to make use of the element. For more information, see [How to: Control the Availability of a Variable](../vs140/How-to--Control-the-Availability-of-a-Variable--Visual-Basic-.md).  
  
## Characteristics of the Elements  
 The following table shows the declared elements and the characteristics that apply to each one.  
  
|Element|Data Type|Lifetime|Scope <sup>1</sup>|Access Level|  
|-------------|---------------|--------------|------------------------|------------------|  
|Variable|Yes|Yes|Yes|Yes|  
|Constant|Yes|No|Yes|Yes|  
|Enumeration|Yes|No|Yes|Yes|  
|Structure|No|No|Yes|Yes|  
|Property|Yes|Yes|Yes|Yes|  
|Method|No|Yes|Yes|Yes|  
|Procedure (`Sub` or `Function`)|No|Yes|Yes|Yes|  
|Procedure parameter|Yes|Yes|Yes|No|  
|Function return|Yes|Yes|Yes|No|  
|Operator|Yes|No|Yes|Yes|  
|Interface|No|No|Yes|Yes|  
|Class|No|No|Yes|Yes|  
|Event|No|No|Yes|Yes|  
|Delegate|No|No|Yes|Yes|  
  
 <sup>1</sup> Scope is sometimes referred to as *visibility*.  
  
## See Also  
 [Declared Elements in Visual Basic](../vs140/Declared-Elements-in-Visual-Basic.md)   
 [Declared Element Names](../vs140/Declared-Element-Names--Visual-Basic-.md)   
 [References to Declared Elements](../vs140/References-to-Declared-Elements--Visual-Basic-.md)   
 [Lifetime in Visual Basic](../vs140/Lifetime-in-Visual-Basic.md)   
 [Scope in Visual Basic](../vs140/Scope-in-Visual-Basic.md)   
 [Access Levels in Visual Basic](../vs140/Access-Levels-in-Visual-Basic.md)   
 [Data Types in Visual Basic](../vs140/Data-Types-in-Visual-Basic.md)   
 [Variable Declaration in Visual Basic](../Topic/Variable%20Declaration%20in%20Visual%20Basic.md)