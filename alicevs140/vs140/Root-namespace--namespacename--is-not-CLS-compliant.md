---
title: "Root namespace &lt;namespacename&gt; is not CLS-compliant"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ec850295-b2fe-4f19-b808-d22fe0aaa32d
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Root namespace &lt;namespacename&gt; is not CLS-compliant
An assembly is marked as `<CLSCompliant(True)>`, but the root namespace name begins with an underscore (`_`).  
  
 A programming element can contain one or more underscores, but to be compliant with the [Common Language Specification](assetId:///4f0b77d0-4844-464f-af73-6e06bedeafc6) (CLS), it must not begin with an underscore. See [Declared Element Names](../vs140/Declared-Element-Names--Visual-Basic-.md).  
  
 When you apply the <xref:System.CLSCompliantAttribute?qualifyHint=False> to a programming element, you set the attribute's `isCompliant` parameter to either `True` or `False` to indicate compliance or noncompliance. There is no default for this parameter, and you must supply a value.  
  
 If you do not apply the <xref:System.CLSCompliantAttribute?qualifyHint=False> to an element, it is considered to be noncompliant.  
  
 By default, this message is a warning. For information on hiding warnings or treating warnings as errors, see [Configuring Warnings in Visual Basic](../vs140/Configuring-Warnings-in-Visual-Basic.md).  
  
 **Error ID:** BC40038  
  
### To correct this error  
  
-   If you require CLS compliance, change the root namespace name so that it does not begin with an underscore.  
  
-   If you require that the root namespace name remain unchanged, then remove the <xref:System.CLSCompliantAttribute?qualifyHint=False> from the assembly or mark it as `<CLSCompliant(False)>`.  
  
## See Also  
 [Namespace Statement](../Topic/Namespace%20Statement.md)   
 [Namespaces in Visual Basic](../Topic/Namespaces%20in%20Visual%20Basic.md)   
 [/rootnamespace](../Topic/-rootnamespace.md)   
 [NIB: How to: Change the Namespace for an Application (Visual Basic)](assetId:///029d85c0-e173-4f7a-afba-a29f3aaf6ebf)   
 [Declared Element Names](../vs140/Declared-Element-Names--Visual-Basic-.md)   
 [Visual Basic Naming Conventions](../Topic/Visual%20Basic%20Naming%20Conventions.md)   
 [<PAVE OVER\> Writing CLS-Compliant Code](assetId:///4c705105-69a2-4e5e-b24e-0633bc32c7f3)