---
title: "Attribute specifier is not a complete statement"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a0ddd673-4170-4bea-9c22-777d7bf21dfd
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Attribute specifier is not a complete statement
Attribute specifier is not a complete statement. Use a line continuation to apply the attribute to the following statement.  
  
 An attribute block appears alone on a source-code line. Attributes must be applied at the beginning of a declaration statement, and they must be part of that statement.  
  
 **Error ID:** BC32035  
  
### To correct this error  
  
-   If the declaration statement is on the following line, add a space and an underscore (`_`) following the attribute block to combine the source-code lines.  
  
-   If no declaration statement is associated with the attribute block, either supply one or remove the attribute block.  
  
-   If the attribute is to apply to the entire assembly or to the current assembly module, the attribute block remains on a separate source-code line. Precede the attribute name inside the angle brackets (`< >`) with `Assembly:` or `Module:` and do not add a space or underscore following the attribute block. Also, be sure this attribute block is at the beginning of your source file.  
  
## See Also  
 [NOT IN BUILD: Application of Attributes](assetId:///2b1703ed-4437-49b3-bc0b-568094324f47)   
 [How to: Break and Combine Statements in Code](../vs140/How-to--Break-and-Combine-Statements-in-Code--Visual-Basic-.md)