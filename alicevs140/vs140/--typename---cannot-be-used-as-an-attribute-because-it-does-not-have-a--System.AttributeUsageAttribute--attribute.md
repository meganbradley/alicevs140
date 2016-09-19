---
title: "&#39;&lt;typename&gt;&#39; cannot be used as an attribute because it does not have a &#39;System.AttributeUsageAttribute&#39; attribute"
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7dd84c9d-6711-4dab-afc6-1fe4dee78051
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;&lt;typename&gt;&#39; cannot be used as an attribute because it does not have a &#39;System.AttributeUsageAttribute&#39; attribute
An attempt was made to use an attribute that was declared without the `System.AttributeUsageAttribute` to define its usage.  
  
 **Error ID:** BC31505  
  
### To correct this error  
  
1.  Custom attributes must be classes derived from`System.Attribute` that have the `AttributeUsageAttribute` attribute applied.  
  
## See Also  
 <xref:System.AttributeUsageAttribute?qualifyHint=False>   
 [NOT IN BUILD: Custom Attributes in Visual Basic](assetId:///d72d8a5c-8f64-4614-b15b-cad66845d047)