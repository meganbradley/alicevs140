---
title: "Declaration Contexts and Default Access Levels (Visual Basic)"
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
ms.assetid: bf63b96e-e825-4745-88c8-5dae222728db
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Declaration Contexts and Default Access Levels (Visual Basic)
This topic describes which Visual Basic types can be declared within which other types, and what their access levels default to if not specified.  
  
## Declaration Context Levels  
 The *declaration context* of a programming element is the region of code in which it is declared. This is often another programming element, which is then called the *containing element*.  
  
 The levels for declaration contexts are the following:  
  
-   *Namespace level* — within a source file or namespace but not within a class, structure, module, or interface  
  
-   *Module level* — within a class, structure, module, or interface but not within a procedure or block  
  
-   *Procedure level* — within a procedure or block (such as `If` or `For`)  
  
 The following table shows the default access levels for various declared programming elements, depending on their declaration contexts.  
  
|Declared element|Namespace level|Module level|Procedure level|  
|----------------------|---------------------|------------------|---------------------|  
|Variable ([Dim Statement](../Topic/Dim%20Statement%20\(Visual%20Basic\).md))|Not allowed|`Private` (`Public` in `Structure`, not allowed in `Interface`)|`Public`|  
|Constant ([Const Statement (Visual Basic)](../Topic/Const%20Statement%20\(Visual%20Basic\).md))|Not allowed|`Private` (`Public` in `Structure`, not allowed in `Interface`)|`Public`|  
|Enumeration ([Enum Statement (Visual Basic)](../Topic/Enum%20Statement%20\(Visual%20Basic\).md))|`Friend`|`Public`|Not allowed|  
|Class ([Class Statement (Visual Basic)](../Topic/Class%20Statement%20\(Visual%20Basic\).md))|`Friend`|`Public`|Not allowed|  
|Structure ([Structure Statement](../Topic/Structure%20Statement.md))|`Friend`|`Public`|Not allowed|  
|Module ([Module Statement](../Topic/Module%20Statement.md))|`Friend`|Not allowed|Not allowed|  
|Interface ([Interface Statement](../vs140/Interface-Statement--Visual-Basic-.md))|`Friend`|`Public`|Not allowed|  
|Procedure ([Function Statement (Visual Basic)](../Topic/Function%20Statement%20\(Visual%20Basic\).md), [Sub Statement (Visual Basic)](../Topic/Sub%20Statement%20\(Visual%20Basic\).md))|Not allowed|`Public`|Not allowed|  
|External reference ([Declare Statement](../Topic/Declare%20Statement.md))|Not allowed|`Public` (not allowed in `Interface`)|Not allowed|  
|Operator ([Operator Statement](../vs140/Operator-Statement.md))|Not allowed|`Public` (not allowed in `Interface` or `Module`)|Not allowed|  
|Property ([Property Statement](../vs140/Property-Statement.md))|Not allowed|`Public`|Not allowed|  
|Default property ([Default (Visual Basic)](../vs140/Default--Visual-Basic-.md))|Not allowed|`Public` (not allowed in `Module`)|Not allowed|  
|Event ([Event Statement](../vs140/Event-Statement.md))|Not allowed|`Public`|Not allowed|  
|Delegate ([Delegate Statement](../vs140/Delegate-Statement.md))|`Friend`|`Public`|Not allowed|  
  
 For more information, see [Access Levels in Visual Basic](../vs140/Access-Levels-in-Visual-Basic.md).  
  
## See Also  
 [Friend (Visual Basic)](../Topic/Friend%20\(Visual%20Basic\).md)   
 [Private (Visual Basic)](../vs140/Private--Visual-Basic-.md)   
 [Public (Visual Basic)](../vs140/Public--Visual-Basic-.md)