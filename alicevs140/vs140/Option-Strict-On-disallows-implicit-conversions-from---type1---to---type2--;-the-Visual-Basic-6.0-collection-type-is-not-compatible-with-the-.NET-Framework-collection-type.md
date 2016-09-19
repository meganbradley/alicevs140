---
title: "Option Strict On disallows implicit conversions from &#39;&lt;type1&gt;&#39; to &#39;&lt;type2&gt;&#39;; the Visual Basic 6.0 collection type is not compatible with the .NET Framework collection type"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7e1bb22e-a507-483e-bfd6-f3a43e24a232
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Option Strict On disallows implicit conversions from &#39;&lt;type1&gt;&#39; to &#39;&lt;type2&gt;&#39;; the Visual Basic 6.0 collection type is not compatible with the .NET Framework collection type
`Option Strict On` disallows implicit conversions from '`<type1>`' to '`<type2>`'; the Visual Basic 6.0 collection type is not compatible with the [!INCLUDE[dnprdnshort](../vs140/includes/dnprdnshort_md.md)] collection type.  
  
 The collection object that is used in Visual Basic 6.0 differs from the collection object that is used in [!INCLUDE[vs_current_long](../vs140/includes/vs_current_long_md.md)].  
  
 **Error ID:** BC30753  
  
### To correct this error  
  
-   Explicitly convert collection objects by using one of the type conversion keywords. The [CType Function](../Topic/CType%20Function%20\(Visual%20Basic\).md) and [DirectCast](../Topic/DirectCast%20Operator%20\(Visual%20Basic\).md) keywords throw a run-time exception if the conversion fails. The [TryCast](../Topic/TryCast%20Operator%20\(Visual%20Basic\).md) keyword returns [Nothing (Visual Basic)](../Topic/Nothing%20\(Visual%20Basic\).md) if the conversion fails.  
  
## See Also  
 [CType Function](../Topic/CType%20Function%20\(Visual%20Basic\).md)   
 [DirectCast](../Topic/DirectCast%20Operator%20\(Visual%20Basic\).md)   
 [TryCast](../Topic/TryCast%20Operator%20\(Visual%20Basic\).md)   
 [Nothing (Visual Basic)](../Topic/Nothing%20\(Visual%20Basic\).md)   
 [NIB Collections in Visual Basic](assetId:///8b2b7845-2251-4573-8dd3-c9f9c0a66a21)