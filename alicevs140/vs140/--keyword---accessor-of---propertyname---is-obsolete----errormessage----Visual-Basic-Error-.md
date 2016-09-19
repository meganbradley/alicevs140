---
title: "&#39;&lt;keyword&gt;&#39; accessor of &#39;&lt;propertyname&gt;&#39; is obsolete: &#39;&lt;errormessage&gt;&#39; (Visual Basic Error)"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b690be0c-4dca-4f79-88ed-4ee3e3f1f90b
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;&lt;keyword&gt;&#39; accessor of &#39;&lt;propertyname&gt;&#39; is obsolete: &#39;&lt;errormessage&gt;&#39; (Visual Basic Error)
A statement attempts to read or write a property for which the corresponding procedure has been marked with the <xref:System.ObsoleteAttribute?qualifyHint=False> attribute and the directive to treat it as an error.  
  
 You can mark any programming element as being no longer in use by applying <xref:System.ObsoleteAttribute?qualifyHint=False> to it. If you do this, you can set the attribute's <xref:System.ObsoleteAttribute.IsError?qualifyHint=False> property to either `True` or `False`. If you set it to `True`, the compiler treats an attempt to use the element as an error. If you set it to `False`, or let it default to `False`, the compiler issues a warning if there is an attempt to use the element.  
  
 **Error ID:** BC30911  
  
### To correct this error  
  
1.  Examine the quoted error message and take appropriate action.  
  
2.  Ensure that the source-code reference is spelling the property name correctly.  
  
3.  Avoid accessing the property in the way (reading or writing) that generated this message.  
  
## See Also  
 [NOT IN BUILD: Attributes Used in Visual Basic](assetId:///22231318-8a40-49af-9245-e0aab723563b)   
 [NOT IN BUILD: Application of Attributes](assetId:///2b1703ed-4437-49b3-bc0b-568094324f47)   
 [Property Procedures](../vs140/Property-Procedures--Visual-Basic-.md)