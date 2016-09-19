---
title: "&#39;&lt;attributename&gt;&#39; cannot be applied more than once to an assembly"
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7312570f-8afb-4afe-992f-b6f7796f5f26
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;&lt;attributename&gt;&#39; cannot be applied more than once to an assembly
The specified attribute can only be applied once to an attribute.  
  
 **Error ID:** BC31521  
  
### To correct this error  
  
1.  Remove redundant applications of this attribute.  
  
2.  If you are using a custom attribute you developed, modify `AttributeUsageAttribute` and set the `AllowMultiple` property to `True`.  
  
## See Also  
 <xref:System.AttributeUsageAttribute?qualifyHint=False>   
 <xref:System.AttributeUsageAttribute.AllowMultiple?qualifyHint=True>