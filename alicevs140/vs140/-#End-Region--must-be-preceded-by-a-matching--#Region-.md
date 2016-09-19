---
title: "&#39;#End Region&#39; must be preceded by a matching &#39;#Region&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1ea60620-c8dc-4957-8cf4-07b25d20da3b
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;#End Region&#39; must be preceded by a matching &#39;#Region&#39;
With `#Region` you can specify a block of code to expand or collapse when using the outlining feature of the [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] Code Editor. The start and end of `#Region` statements must be in the same code block.  
  
 **Error ID:** BC30680  
  
### To correct this error  
  
-   Insert `#Region` at the appropriate place before the corresponding `#End``Region` statement.  
  
## See Also  
 [#Region Directive](../vs140/#Region-Directive.md)