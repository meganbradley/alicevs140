---
title: "Class &#39;&lt;classname&gt;&#39; should declare a &#39;Sub New&#39; because the &#39;&lt;constructorname&gt;&#39; in its base class &#39;&lt;baseclassname&gt;&#39; is marked obsolete"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b2c6b996-6d52-4963-9fee-8b6f78fc028c
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Class &#39;&lt;classname&gt;&#39; should declare a &#39;Sub New&#39; because the &#39;&lt;constructorname&gt;&#39; in its base class &#39;&lt;baseclassname&gt;&#39; is marked obsolete
A class declaration does not include a constructor, and the base class constructor is marked with the <xref:System.ObsoleteAttribute?qualifyHint=False> attribute and the directive to treat it as a warning.  
  
 When a derived class does not declare a constructor, [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] attempts to generate an implicit parameterless constructor that calls `MyBase.New()`. If there is no accessible constructor in the base class that can be called without arguments, [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] cannot generate an implicit constructor. In this case, the required constructor is marked with the <xref:System.ObsoleteAttribute?qualifyHint=False> attribute, so [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] cannot call it.  
  
 You can mark any programming element as being no longer in use by applying <xref:System.ObsoleteAttribute?qualifyHint=False> to it. If you do this, you can set the attribute's <xref:System.ObsoleteAttribute.IsError?qualifyHint=False> property to either `True` or `False`. If you set it to `True`, the compiler treats an attempt to use the element as an error. If you set it to `False`, or let it default to `False`, the compiler issues a warning if there is an attempt to use the element.  
  
 By default, this message is a warning, because the <xref:System.ObsoleteAttribute.IsError?qualifyHint=False> property of <xref:System.ObsoleteAttribute?qualifyHint=False> is `False`. For information on hiding warnings or treating warnings as errors, see [Configuring Warnings in Visual Basic](../vs140/Configuring-Warnings-in-Visual-Basic.md).  
  
 **Error ID:** BC41001  
  
### To correct this error  
  
1.  Use `Sub New` to declare a constructor in the derived class.  
  
## See Also  
 [NOT IN BUILD: Attributes Used in Visual Basic](assetId:///22231318-8a40-49af-9245-e0aab723563b)   
 [NOT IN BUILD: Application of Attributes](assetId:///2b1703ed-4437-49b3-bc0b-568094324f47)