---
title: "Implementing class &#39;&lt;underlyingclassname&gt;&#39; for interface &#39;&lt;interfacename&gt;&#39; is not accessible in this context because it is &#39;&lt;accesslevel&gt;&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ab2a3bc3-b875-476f-b601-3e736ad2677e
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Implementing class &#39;&lt;underlyingclassname&gt;&#39; for interface &#39;&lt;interfacename&gt;&#39; is not accessible in this context because it is &#39;&lt;accesslevel&gt;&#39;
An interface is declared with the <xref:System.Runtime.InteropServices.CoClassAttribute?qualifyHint=False> specifying an underlying class, but that class has an access level that prevents the using code from accessing it.  
  
 Applying the <xref:System.Runtime.InteropServices.CoClassAttribute?qualifyHint=False> to an interface associates an underlying class with the interface. This allows code to create an object directly from the interface using a `New` clause.  
  
 If the code using the `New` clause does not have access to the underlying class, for example if the class is `Private`, then the compiler generates this error.  
  
 **Error ID:** BC31109  
  
### To correct this error  
  
1.  If you have source control over the underlying class, then adjust its access level so the using code can access it.  
  
2.  If for any reason you cannot change the access level of the underlying class, then remove the `New` clause. You cannot create an object directly from this interface.  
  
## See Also  
 <xref:System.Runtime.InteropServices.CoClassAttribute?qualifyHint=False>   
 [New (Visual Basic)](../vs140/New-Operator--Visual-Basic-.md)   
 [Access Levels in Visual Basic](../vs140/Access-Levels-in-Visual-Basic.md)