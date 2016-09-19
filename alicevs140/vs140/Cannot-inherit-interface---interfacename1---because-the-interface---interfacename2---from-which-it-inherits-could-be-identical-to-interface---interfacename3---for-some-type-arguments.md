---
title: "Cannot inherit interface &#39;&lt;interfacename1&gt;&#39; because the interface &#39;&lt;interfacename2&gt;&#39; from which it inherits could be identical to interface &#39;&lt;interfacename3&gt;&#39; for some type arguments"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 56b1167e-f626-4a27-8395-9d396cc209f2
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Cannot inherit interface &#39;&lt;interfacename1&gt;&#39; because the interface &#39;&lt;interfacename2&gt;&#39; from which it inherits could be identical to interface &#39;&lt;interfacename3&gt;&#39; for some type arguments
A generic interface inherits from two or more generic interfaces, and two of the inheritances could conflict for certain values of type arguments.  
  
 The following statements can generate this error.  
  
```  
Public Interface interfaceA(Of u)  
    Inherits interfaceX(Of u)  
End Interface  
Public Interface interfaceX(Of v)  
End Interface  
Public Interface derivedInterface(Of t1, t2)  
    Inherits interfaceA(Of t1), interfaceX(Of t2)  
End Interface  
```  
  
 If `derivedInterface` is constructed or implemented supplying the same type to both `t1` and `t2`, it must inherit two versions of `interfaceX` with identical type arguments. Doing so would produce an ambiguity about which version to access.  
  
 **Error ID:** BC32121  
  
### To correct this error  
  
-   Change one of the type arguments supplied to the derived interface so that there is no conflict.  
  
     -or-  
  
-   Remove from the `Inherits` statement one of the interfaces causing the potential inheritance or implementation conflict.  
  
## See Also  
 [NOT IN BUILD: Interfaces Overview](assetId:///f96bb470-c1b8-4c73-89bc-6f536b798da1)   
 [Interface Statement (Visual Basic)](../vs140/Interface-Statement--Visual-Basic-.md)   
 [Inheritance Basics](../vs140/Inheritance-Basics--Visual-Basic-.md)   
 [Inherits Statement](../vs140/Inherits-Statement.md)   
 [Generic Types in Visual Basic](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)