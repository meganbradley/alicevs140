---
title: "&#39;&lt;expression&gt;&#39; cannot be used as a type constraint"
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
ms.assetid: b17821b7-fa14-4397-a211-6e2a14079f09
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;&lt;expression&gt;&#39; cannot be used as a type constraint
A constraint list includes an expression that does not represent a valid constraint on a type parameter.  
  
 A constraint list imposes requirements on the type argument passed to the type parameter. You can specify the following requirements in any combination:  
  
-   The type argument must implement one or more interfaces  
  
-   The type argument must inherit from at most one class  
  
-   The type argument must expose a parameterless constructor that the creating code can access (include the `New` constraint)  
  
 If you do not include any specific class or interface in the constraint list, you can impose a more general requirement by specifying one of the following:  
  
-   The type argument must be a value type (include the `Structure` constraint)  
  
-   The type argument must be a reference type (include the `Class` constraint)  
  
 You cannot specify both `Structure` and `Class` for the same type parameter, and you cannot specify either one more than once.  
  
 **Error ID:** BC32061  
  
### To correct this error  
  
-   Verify that the expression and its elements are spelled correctly.  
  
-   If the expression does not qualify for the preceding list of requirements, remove it from the constraint list.  
  
-   If the expression refers to an interface or class, verify that the compiler has access to that interface or class. You might need to qualify its name, and you might need to add a reference to your project. For more information, see "References to Projects" in [References to Declared Elements](../vs140/References-to-Declared-Elements--Visual-Basic-.md).  
  
## See Also  
 [Generic Types in Visual Basic](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)   
 [Value Types and Reference Types](../Topic/Value%20Types%20and%20Reference%20Types.md)   
 [References to Declared Elements](../vs140/References-to-Declared-Elements--Visual-Basic-.md)   
 [NIB How to: Add or Remove References By Using the Add Reference Dialog Box](assetId:///3bd75d61-f00c-47c0-86a2-dd1f20e231c9)