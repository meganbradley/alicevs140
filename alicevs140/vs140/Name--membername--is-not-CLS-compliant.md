---
title: "Name &lt;membername&gt; is not CLS-compliant"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-visual-basic
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e2b885dc-cbf9-49ff-bbbe-531657ea99f7
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Name &lt;membername&gt; is not CLS-compliant
An assembly is marked as `<CLSCompliant(True)>` but exposes a member with a name that begins with an underscore (`_`).  
  
 A programming element can contain one or more underscores, but to be compliant with the [Common Language Specification](assetId:///4f0b77d0-4844-464f-af73-6e06bedeafc6) (CLS), it must not begin with an underscore. See [Declared Element Names](../vs140/Declared-Element-Names--Visual-Basic-.md).  
  
 When you apply the <xref:System.CLSCompliantAttribute?qualifyHint=False> to a programming element, you set the attribute's `isCompliant` parameter to either `True` or `False` to indicate compliance or noncompliance. There is no default for this parameter, and you must supply a value.  
  
 If you do not apply the <xref:System.CLSCompliantAttribute?qualifyHint=False> to an element, it is considered to be noncompliant.  
  
 By default, this message is a warning. For information on hiding warnings or treating warnings as errors, see [Configuring Warnings in Visual Basic](../vs140/Configuring-Warnings-in-Visual-Basic.md).  
  
 **Error ID:** BC40031  
  
### To correct this error  
  
-   If you have control over the source code, change the member name so that it does not begin with an underscore.  
  
-   If you require that the member name remain unchanged, remove the <xref:System.CLSCompliantAttribute?qualifyHint=False> from its definition or mark it as `<CLSCompliant(False)>`. You can still mark the assembly as `<CLSCompliant(True)>`.  
  
## See Also  
 [Declared Element Names](../vs140/Declared-Element-Names--Visual-Basic-.md)   
 [Visual Basic Naming Conventions](../Topic/Visual%20Basic%20Naming%20Conventions.md)   
 [<PAVE OVER\> Writing CLS-Compliant Code](assetId:///4c705105-69a2-4e5e-b24e-0633bc32c7f3)