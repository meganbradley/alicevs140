---
title: "Generic type &#39;&lt;generictypename&gt;&#39; cannot be imported more than once"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d93bae4b-3224-4a6e-a072-8ce231084519
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Generic type &#39;&lt;generictypename&gt;&#39; cannot be imported more than once
An [Imports Statement](../Topic/Imports%20Statement%20\(.NET%20Namespace%20and%20Type\).md) specifies a generic type that has already been imported with different type parameterization.  
  
 You can declare multiple constructed types from a generic type, because you do not redefine the generic type by declaring a constructed type. However, if you import a generic type more than once, that is the equivalent of multiple definitions.  
  
 **Error ID:** BC32086  
  
### To correct this error  
  
1.  If the source file containing this `Imports` statement also contains another `Imports` statement specifying the same generic type, remove one of them.  
  
2.  If you need to import the same generic type with different type parameterizations, use multiple source files.  
  
## See Also  
 [Generic Types in Visual Basic](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)