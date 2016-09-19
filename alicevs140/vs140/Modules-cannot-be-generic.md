---
title: "Modules cannot be generic"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 47246e2b-51d4-4a10-a3ac-bc77b44fa2ca
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Modules cannot be generic
A `Module` statement uses the `Of` keyword to introduce generic type parameters.  
  
 You can define and use generic classes, structures, interfaces, procedures, and delegates. You cannot define generic modules.  
  
 **Error ID:** BC32073  
  
### To correct this error  
  
1.  Remove the `Of` keyword from the `Module` statement.  
  
2.  If you want the functionality of a generic module, the closest approximation is a generic class. Use a [Class Statement (Visual Basic)](../Topic/Class%20Statement%20\(Visual%20Basic\).md) instead of a `Module` statement.  
  
## See Also  
 [Module Statement](../Topic/Module%20Statement.md)   
 [Of](../Topic/Of%20Clause%20\(Visual%20Basic\).md)   
 [Generic Types in Visual Basic](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)   
 [How to: Define a Class That Can Provide Identical Functionality on Different Data Types](../vs140/How-to--Define-a-Class-That-Can-Provide-Identical-Functionality-on-Different-Data-Types--Visual-Basic-.md)