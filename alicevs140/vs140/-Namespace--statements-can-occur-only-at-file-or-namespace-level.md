---
title: "&#39;Namespace&#39; statements can occur only at file or namespace level"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: bcd365a4-5d84-4c3c-83dc-40cb4c47f73b
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;Namespace&#39; statements can occur only at file or namespace level
`Namespace` statements must appear after `Option` statements, `Imports` statements, and global attributes, but before all other declarations in your source file.  
  
 **Error ID:** BC30618  
  
### To correct this error  
  
-   Move the `Namespace` statement to the top of your namespace declaration or source file.  
  
## See Also  
 [Namespace Statement](../Topic/Namespace%20Statement.md)   
 [Namespaces in Visual Basic](../Topic/Namespaces%20in%20Visual%20Basic.md)