---
title: "Indirect constraint &#39;&lt;constraint1&gt;&#39; obtained from the type parameter constraint &#39;&lt;typeparameter1&gt;&#39; conflicts with the constraint &#39;&lt;constraint2&gt;&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b03b5840-5318-4844-b2da-1bca4c28d097
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Indirect constraint &#39;&lt;constraint1&gt;&#39; obtained from the type parameter constraint &#39;&lt;typeparameter1&gt;&#39; conflicts with the constraint &#39;&lt;constraint2&gt;&#39;
A generic type is declared with conflicting constraints due to a combination of direct and indirect constraints.  
  
 The following statement can generate this error.  
  
 `Public Class testClass(Of t1 As {t2, Class}, t2 As Structure)`  
  
 The indirect constraint `Structure` and the direct constraint `Class` cause a conflict for type parameter `t1`, because the `Structure` constraint requires that the corresponding type argument be a value type, while `Class` requires that it be a reference type.  
  
 **Error ID:** BC32111  
  
### To correct this error  
  
-   Change the type parameter constraints to avoid conflicting constraints.  
  
## See Also  
 [Generic Types in Visual Basic](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)   
 [Type List](../vs140/Type-List--Visual-Basic-.md)   
 [Structure (Visual Basic)](assetId:///263ce115-ac36-4c05-8cb7-0e0eead5c6d0)   
 [Class (Visual Basic)](assetId:///0777c6e6-46bc-451b-ad70-57b49d4ef4f7)   
 [Value Types and Reference Types](../Topic/Value%20Types%20and%20Reference%20Types.md)