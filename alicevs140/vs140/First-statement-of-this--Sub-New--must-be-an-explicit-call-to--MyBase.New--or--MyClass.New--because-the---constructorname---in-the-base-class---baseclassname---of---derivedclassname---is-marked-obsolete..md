---
title: "First statement of this &#39;Sub New&#39; must be an explicit call to &#39;MyBase.New&#39; or &#39;MyClass.New&#39; because the &#39;&lt;constructorname&gt;&#39; in the base class &#39;&lt;baseclassname&gt;&#39; of &#39;&lt;derivedclassname&gt;&#39; is marked obsolete."
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 437e3204-8ddc-45d3-b9b4-c66d53a61a6d
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# First statement of this &#39;Sub New&#39; must be an explicit call to &#39;MyBase.New&#39; or &#39;MyClass.New&#39; because the &#39;&lt;constructorname&gt;&#39; in the base class &#39;&lt;baseclassname&gt;&#39; of &#39;&lt;derivedclassname&gt;&#39; is marked obsolete.
A class constructor does not explicitly call a base class constructor, and the implicit base class constructor is marked with the <xref:System.ObsoleteAttribute?qualifyHint=False> attribute and the directive to treat it as an error.  
  
 When a derived class constructor does not call a base class constructor, [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] attempts to generate an implicit call to a parameterless base class constructor. If there is no accessible constructor in the base class that can be called without arguments, [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] cannot generate an implicit call. In this case, the required constructor is marked with the <xref:System.ObsoleteAttribute?qualifyHint=False> attribute, so [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] cannot call it.  
  
 You can mark any programming element as being no longer in use by applying <xref:System.ObsoleteAttribute?qualifyHint=False> to it. If you do this, you can set the attribute's <xref:System.ObsoleteAttribute.IsError?qualifyHint=False> property to either `True` or `False`. If you set it to `True`, the compiler treats an attempt to use the element as an error. If you set it to `False`, or let it default to `False`, the compiler issues a warning if there is an attempt to use the element.  
  
 **Error ID:** BC30919  
  
### To correct this error  
  
-   Include a call to `MyBase.New()` or `MyClass.New()` as the first statement of the `Sub New` in the derived class.  
  
## See Also  
 [NOT IN BUILD: Attributes Used in Visual Basic](assetId:///22231318-8a40-49af-9245-e0aab723563b)   
 [NOT IN BUILD: Application of Attributes](assetId:///2b1703ed-4437-49b3-bc0b-568094324f47)