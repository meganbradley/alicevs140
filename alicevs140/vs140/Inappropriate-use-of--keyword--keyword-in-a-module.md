---
title: "Inappropriate use of &lt;keyword&gt; keyword in a module"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a9bc1e9d-ba2c-4a71-b147-0fb66f670316
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Inappropriate use of &lt;keyword&gt; keyword in a module
Modules do not have instances, support inheritance, or implement interfaces. Therefore, the following keywords do not apply to a module declaration:  
  
-   [MustInherit](../Topic/MustInherit%20\(Visual%20Basic\).md)  
  
-   [NotInheritable](../vs140/NotInheritable--Visual-Basic-.md)  
  
-   [Overloads](../vs140/Overloads--Visual-Basic-.md)  
  
-   [Private (Visual Basic)](../vs140/Private--Visual-Basic-.md)  
  
-   [Protected (Visual Basic)](../vs140/Protected--Visual-Basic-.md)  
  
-   [Shadows](../vs140/Shadows--Visual-Basic-.md)  
  
-   [Shared (Visual Basic)](../Topic/Shared%20\(Visual%20Basic\).md)  
  
-   [Static (Visual Basic)](../vs140/Static--Visual-Basic-.md)  
  
 The only keywords supported in a [Module Statement](../Topic/Module%20Statement.md) are [Public (Visual Basic)](../vs140/Public--Visual-Basic-.md) and [Friend (Visual Basic)](../Topic/Friend%20\(Visual%20Basic\).md).  
  
 In addition, you cannot use the [Implements (Visual Basic)](../vs140/Implements-Clause--Visual-Basic-.md) statement or the [Inherits Statement](../vs140/Inherits-Statement.md) in the statement block of the module.  
  
 By default, this message is a warning. For more information about how to hide warnings or treat warnings as errors, see [Configuring Warnings in Visual Basic](../vs140/Configuring-Warnings-in-Visual-Basic.md).  
  
 **Error ID:** BC42028  
  
### To correct this error  
  
-   If you intend this programming element to be a module, use only the `Public` or `Friend` keyword in its declaration. By default, a module uses to `Friend` if you do not specify its access level.  
  
-   If you intend to create instances of this programming element, declare it as a class. You can then use the keywords that apply to a class declaration.  
  
## See Also  
 [Class Statement (Visual Basic)](../Topic/Class%20Statement%20\(Visual%20Basic\).md)