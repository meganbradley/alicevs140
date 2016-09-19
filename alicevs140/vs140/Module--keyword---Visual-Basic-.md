---
title: "Module &lt;keyword&gt; (Visual Basic)"
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
ms.assetid: d971b940-05ab-4d56-8485-e3b8a661906b
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Module &lt;keyword&gt; (Visual Basic)
Specifies that an attribute at the beginning of a source file applies to the current assembly module.  
  
## Remarks  
 Many attributes pertain to an individual programming element, such as a class or property. You apply such an attribute by attaching the attribute block, within angle brackets (`< >`), directly to the declaration statement.  
  
 If an attribute pertains not only to the following element but to the current assembly module, you place the attribute block at the beginning of the source file and identify the attribute with the `Module` keyword. If it applies to the entire assembly, you use the [Assembly](../vs140/Assembly--Visual-Basic-.md) keyword.  
  
 The `Module` modifier is not the same as the [Module Statement](../Topic/Module%20Statement.md).  
  
## See Also  
 [Assembly](../vs140/Assembly--Visual-Basic-.md)   
 [Module Statement](../Topic/Module%20Statement.md)   
 [Attributes (C# and Visual Basic)](../vs140/Attributes--C#-and-Visual-Basic-.md)