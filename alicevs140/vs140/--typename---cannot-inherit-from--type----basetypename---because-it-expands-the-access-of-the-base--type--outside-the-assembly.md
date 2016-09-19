---
title: "&#39;&lt;typename&gt;&#39; cannot inherit from &lt;type&gt; &#39;&lt;basetypename&gt;&#39; because it expands the access of the base &lt;type&gt; outside the assembly"
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
ms.assetid: 68fc05c5-5d55-4742-9a3b-ea04312594f4
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;&lt;typename&gt;&#39; cannot inherit from &lt;type&gt; &#39;&lt;basetypename&gt;&#39; because it expands the access of the base &lt;type&gt; outside the assembly
A class or interface inherits from a base class or interface but has a less restrictive access level.  
  
 For example, a `Public` interface inherits from a `Friend` interface, or a `Protected` class inherits from a `Private` class. This exposes the base class or interface to access beyond the intended level.  
  
 **Error ID:** BC30910  
  
### To correct this error  
  
-   Change the access level of the derived class or interface to be at least as restrictive as that of the base class or interface.  
  
     -or-  
  
-   If you require the less restrictive access level, remove the `Inherits` statement. You cannot inherit from a more restricted base class or interface.  
  
## See Also  
 [Class Statement (Visual Basic)](../Topic/Class%20Statement%20\(Visual%20Basic\).md)   
 [Interface Statement (Visual Basic)](../vs140/Interface-Statement--Visual-Basic-.md)   
 [Inherits Statement](../vs140/Inherits-Statement.md)   
 [Access Levels in Visual Basic](../vs140/Access-Levels-in-Visual-Basic.md)