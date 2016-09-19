---
title: "Non-shared members in a Structure cannot be declared &#39;New&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8e4e1ad8-3bac-475f-82e8-e4f134692204
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Non-shared members in a Structure cannot be declared &#39;New&#39;
A nonshared variable in a structure is declared with a `New` clause.  
  
 You can initialize a shared reference variable in a structure, and you can have a nonshared reference variable without initialization, as the following code lines show.  
  
 `Shared structVar1 As New System.ApplicationException`  
  
 `Dim structVar2 As System.ApplicationException`  
  
 However, you cannot initialize a nonshared reference variable in a structure. The following code line is invalid.  
  
 `Dim structVar3 As New System.ApplicationException ' INVALID IN A STRUCTURE`  
  
 **Error ID:** BC30795  
  
### To correct this error  
  
-   Remove either the `Shared` modifier or the `New` keyword from the reference variable declaration.  
  
## See Also  
 [Structure Statement](../Topic/Structure%20Statement.md)   
 [Shared (Visual Basic)](../Topic/Shared%20\(Visual%20Basic\).md)   
 [New (Visual Basic)](../vs140/New-Operator--Visual-Basic-.md)