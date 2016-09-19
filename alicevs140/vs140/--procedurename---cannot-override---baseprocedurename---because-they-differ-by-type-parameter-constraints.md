---
title: "&#39;&lt;procedurename&gt;&#39; cannot override &#39;&lt;baseprocedurename&gt;&#39; because they differ by type parameter constraints"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9be1a88d-c1a4-4f12-8e72-74abb2be565d
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;&lt;procedurename&gt;&#39; cannot override &#39;&lt;baseprocedurename&gt;&#39; because they differ by type parameter constraints
A generic procedure attempts to override a generic base class procedure, but they have different constraint lists on their type parameters.  
  
 To override a base class procedure, the overriding procedure must match not only the complete signature of the base class procedure, but also the access level of the procedure and the passing mechanism of each parameter.  
  
 To override a generic base class procedure, the overriding procedure must additionally match the number of type parameters and the constraint list of each one.  
  
 For more information on overriding requirements, see [Overrides](../vs140/Overrides--Visual-Basic-.md).  
  
 **Error ID:** BC32077  
  
### To correct this error  
  
-   If you intend to override the base class procedure, revise the type parameter constraints to exactly match those of the base class procedure.  
  
-   If the type parameter constraints must remain as you have them, you cannot override the base class procedure. Remove the `Overrides` keyword from the declaration.  
  
## See Also  
 [Generic Types in Visual Basic](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)