---
title: "Type parameter &#39;&lt;typeparametername1&gt;&#39; must have either a &#39;New&#39; constraint or a &#39;Structure&#39; constraint to satisfy the &#39;New&#39; constraint for type parameter &#39;&lt;typeparametername2&gt;&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a7ff58d3-8c67-40e4-9fd8-92cc00524c22
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Type parameter &#39;&lt;typeparametername1&gt;&#39; must have either a &#39;New&#39; constraint or a &#39;Structure&#39; constraint to satisfy the &#39;New&#39; constraint for type parameter &#39;&lt;typeparametername2&gt;&#39;
A statement constructs a generic type passing a type parameter that is not constrained to satisfy a `New` constraint.  
  
 The `New` constraint means that the type argument supplied to that type parameter must expose a parameterless constructor accessible to the code that creates objects from it. All value types have parameterless constructors, but not all reference types do. Therefore the `Structure` constraint satisfies the `New` constraint, but the `Class` constraint, or a class or interface name, does not.  
  
 The following statements can generate this error.  
  
```  
Public Class c1(Of t As New)  
End Class  
Public Class c2(Of u)  
    Public testObject As New c1(Of u)  
End Class  
```  
  
 When class `c2` creates an object from `c1`, type parameter `u` does not satisfy the `New` constraint on type parameter `t`.  
  
 **Error ID:** BC32084  
  
### To correct this error  
  
-   If the type parameter to be passed to the generic type can satisfy the `Structure` or `New` constraint, then add the appropriate constraint to its definition.  
  
    ```  
    Public Class c2(Of u As Structure)  
    ```  
  
-   If the type parameter cannot satisfy the `Structure` or `New` constraint, then do not pass it to the generic type. You must pass something else as the type argument.  
  
## See Also  
 [Generic Types in Visual Basic](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)   
 [New (Visual Basic)](../vs140/New-Operator--Visual-Basic-.md)   
 [Structure (Visual Basic)](assetId:///263ce115-ac36-4c05-8cb7-0e0eead5c6d0)   
 [Class (Visual Basic)](assetId:///0777c6e6-46bc-451b-ad70-57b49d4ef4f7)   
 [Value Types and Reference Types](../Topic/Value%20Types%20and%20Reference%20Types.md)