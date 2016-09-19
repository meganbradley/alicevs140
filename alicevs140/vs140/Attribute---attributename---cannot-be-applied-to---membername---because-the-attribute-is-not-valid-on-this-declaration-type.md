---
title: "Attribute &#39;&lt;attributename&gt;&#39; cannot be applied to &#39;&lt;membername&gt;&#39; because the attribute is not valid on this declaration type"
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5cd07950-37d0-45e9-8770-3eaac54ff7d9
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Attribute &#39;&lt;attributename&gt;&#39; cannot be applied to &#39;&lt;membername&gt;&#39; because the attribute is not valid on this declaration type
The attribute you are using is not appropriate for the item you are using.  
  
 **Error ID:** BC30662  
  
### To correct this error  
  
1.  Choose an attribute that is intended for the item you are using. For example, if you are using method, choose an attribute designed to be used with methods.  
  
2.  If you are using custom attributes that you developed, change the `AttributeUsage` attribute to match the kind of item you are using.  
  
## See Also  
 <xref:System.AttributeUsageAttribute?qualifyHint=False>   
 [NOT IN BUILD: Attributes in Visual Basic](assetId:///620bfc0e-4582-4c8b-8432-ebc5c3dccc22)   
 [NOT IN BUILD: Custom Attributes in Visual Basic](assetId:///d72d8a5c-8f64-4614-b15b-cad66845d047)