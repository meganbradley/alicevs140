---
title: "&#39;New&#39; constraint and &#39;Structure&#39; constraint cannot be combined"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5418b420-a014-4006-84aa-20ddac6739e6
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;New&#39; constraint and &#39;Structure&#39; constraint cannot be combined
A constraint list includes both the [New (Visual Basic)](../vs140/New-Operator--Visual-Basic-.md) constraint and the [Structure (Visual Basic)](assetId:///263ce115-ac36-4c05-8cb7-0e0eead5c6d0) constraint.  
  
 A constraint list on a type parameter can specify that the type argument passed to that type parameter must be a value type (with the `Structure` constraint) or must be a reference type (with the [Class (Visual Basic)](assetId:///0777c6e6-46bc-451b-ad70-57b49d4ef4f7) constraint). You cannot specify both constraints on the same type parameter, and you cannot specify either one more than once.  
  
 The `New` constraint specifies that the type argument must expose a parameterless constructor that the creating code can access. However, a structure cannot have a nonshared parameterless constructor. Therefore, the `New` and `Structure` constraints are in conflict.  
  
 **Error ID:** BC32103  
  
### To correct this error  
  
1.  Decide whether you want to require a value type or a reference type for the type argument.  
  
2.  If you want the type argument to be a value type, remove the `New` keyword from the constraint list.  
  
3.  If you want the type argument to be a reference type, remove the `Structure` keyword from the constraint list.  
  
## See Also  
 [Generic Types in Visual Basic](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)   
 [Value Types and Reference Types](../Topic/Value%20Types%20and%20Reference%20Types.md)