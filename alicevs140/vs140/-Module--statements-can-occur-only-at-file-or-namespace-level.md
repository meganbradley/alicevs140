---
title: "&#39;Module&#39; statements can occur only at file or namespace level"
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
ms.assetid: 5e9de8e5-d26b-4fb2-9e28-814413fe9cef
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;Module&#39; statements can occur only at file or namespace level
`Module` statements must appear at the top of your source file immediately after `Option` and `Imports` statements, global attributes, and namespace declarations, but before all other declarations.  
  
 **Error ID:** BC30617  
  
### To correct this error  
  
-   Move the `Module` statement to the top of your namespace declaration or source file.  
  
## See Also  
 [Module Statement](../Topic/Module%20Statement.md)