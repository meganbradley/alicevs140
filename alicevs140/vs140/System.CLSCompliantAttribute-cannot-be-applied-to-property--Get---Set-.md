---
title: "System.CLSCompliantAttribute cannot be applied to property &#39;Get&#39;-&#39;Set&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
H1: System.CLSCompliantAttribute cannot be applied to property &#39;Get&#39;/&#39;Set&#39;
ms.assetid: 2ff45c09-32be-4ca9-b42a-63ce2536db7d
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# System.CLSCompliantAttribute cannot be applied to property &#39;Get&#39;-&#39;Set&#39;
A property definition applies the <xref:System.CLSCompliantAttribute?qualifyHint=False> attribute to its `Get` or `Set` statement.  
  
 For a property to be compliant with the [Common Language Specification](assetId:///4f0b77d0-4844-464f-af73-6e06bedeafc6) (CLS), the entire property must be marked as `<CLSCompliant(True)>`. You must apply <xref:System.CLSCompliantAttribute?qualifyHint=False> to the [Property Statement](../vs140/Property-Statement.md), not to either the `Get` or the `Set` statement.  
  
 When you apply <xref:System.CLSCompliantAttribute?qualifyHint=False> to a programming element, you set the attribute's `isCompliant` parameter to either `True` or `False` to indicate compliance or noncompliance. There is no default for this parameter, and you must supply a value.  
  
 If you do not apply <xref:System.CLSCompliantAttribute?qualifyHint=False> to an element, it is considered to be noncompliant.  
  
 By default, this message is a warning. For information on hiding warnings or treating warnings as errors, see [Configuring Warnings in Visual Basic](../vs140/Configuring-Warnings-in-Visual-Basic.md).  
  
 **Error ID:** BC40043  
  
### To correct this error  
  
-   Remove <xref:System.CLSCompliantAttribute?qualifyHint=False> from the `Get` or `Set` statement.  
  
-   If the property should be CLS-compliant, mark the `Property` statement as `<CLSCompliant(True)>`.  
  
## See Also  
 [<PAVE OVER\> Writing CLS-Compliant Code](assetId:///4c705105-69a2-4e5e-b24e-0633bc32c7f3)   
 [Get Statement](../vs140/Get-Statement.md)   
 [Set Statement (Visual Basic)](../vs140/Set-Statement--Visual-Basic-.md)