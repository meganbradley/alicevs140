---
title: "#Region Directive"
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
ms.assetid: 90a6a104-3cbf-47d0-bdc4-b585d0921b87
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# #Region Directive
Collapses and hides sections of code in Visual Basic files.  
  
## Syntax  
  
```  
  
      #Region "identifier_string"  
#End Region  
```  
  
## Parts  
  
|||  
|-|-|  
|Term|Definition|  
|`identifier_string`|Required. String that acts as the title of a region when it is collapsed. Regions are collapsed by default.|  
|`#End Region`|Terminates the `#Region` block.|  
  
## Remarks  
 Use the `#Region` directive to specify a block of code to expand or collapse when using the outlining feature of the Visual Studio Code Editor. You can place, or *nest*, regions within other regions to group similar regions together.  
  
## Example  
 This example uses the `#Region` directive.  
  
 [!CODE [VbVbalrConditionalComp#4](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrConditionalComp#4)]  
  
## See Also  
 [#If...Then...#Else Directives](../vs140/#If...Then...#Else-Directives.md)   
 [Outlining](../vs140/Outlining.md)   
 [How to: Collapse and Hide Sections of Code](../vs140/How-to--Collapse-and-Hide-Sections-of-Code--Visual-Basic-.md)