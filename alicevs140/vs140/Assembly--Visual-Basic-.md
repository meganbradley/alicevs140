---
title: "Assembly (Visual Basic)"
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
ms.assetid: 925e7471-3bdf-4b51-bb93-cbcfc6efc52f
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Assembly (Visual Basic)
Specifies that an attribute at the beginning of a source file applies to the entire assembly.  
  
## Remarks  
 Many attributes pertain to an individual programming element, such as a class or property. You apply such an attribute by attaching the attribute block, within angle brackets (`< >`), directly to the declaration statement.  
  
 If an attribute pertains not only to the following element but to the entire assembly, you place the attribute block at the beginning of the source file and identify the attribute with the `Assembly` keyword. If it applies to the current assembly module, you use the [Module](../vs140/Module--keyword---Visual-Basic-.md) keyword.  
  
 You can also apply an attribute to an assembly in the AssemblyInfo.vb file, in which case you do not have to use an attribute block in your main source-code file.  
  
## See Also  
 [Module <keyword\>](../vs140/Module--keyword---Visual-Basic-.md)   
 [Attributes (C# and Visual Basic)](../vs140/Attributes--C#-and-Visual-Basic-.md)