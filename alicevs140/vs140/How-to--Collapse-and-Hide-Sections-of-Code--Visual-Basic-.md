---
title: "How to: Collapse and Hide Sections of Code (Visual Basic)"
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
ms.assetid: b770e8f5-e07d-491a-ab4b-a977980f9ba2
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Collapse and Hide Sections of Code (Visual Basic)
The `#Region` directive enables you to collapse and hide sections of code in [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] files. The `#Region` directive lets you specify a block of code that you can expand or collapse when using the [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] code editor. The ability to hide code selectively makes your files more manageable and easier to read. For more information, see [Outlining](../vs140/Outlining.md).  
  
 `#Region` directives support code block semantics such as `#If...#End If`. This means they cannot begin in one block and end in another; the start and end must be in the same block. `#Region` directives are not supported within functions.  
  
### To collapse and hide a section of code  
  
-   Place the section of code between the `#Region` and `#End Region` statements, as in the following example:  
  
     [!CODE [VbVbalrConditionalComp#6](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrConditionalComp#6)]  
  
     The `#Region` block can be used multiple times in a code file; thus, users can define their own blocks of procedures and classes that can, in turn, be collapsed. `#Region` blocks can also be nested within other `#Region` blocks.  
  
    > [!NOTE]
    >  Hiding code does not prevent it from being compiled and does not affect `#If...#End If` statements.  
  
## See Also  
 [Conditional Compilation](../vs140/Conditional-Compilation-in-Visual-Basic.md)   
 [#Region Directive](../vs140/#Region-Directive.md)   
 [#If...Then...#Else Directives](../vs140/#If...Then...#Else-Directives.md)   
 [Outlining](../vs140/Outlining.md)