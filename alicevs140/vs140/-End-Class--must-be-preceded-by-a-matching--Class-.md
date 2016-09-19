---
title: "&#39;End Class&#39; must be preceded by a matching &#39;Class&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0e6989da-f281-4ac4-8579-b6d627be8de8
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;End Class&#39; must be preceded by a matching &#39;Class&#39;
`End Class` is used to complete a `Class` block; hence it can only appear at the end of the block. Either you have a redundant `End Class`, or your `End Class` statement appears outside the bounds of its corresponding `Class` block.  
  
 **Error ID:** BC30460  
  
### To correct this error  
  
-   Locate and remove any redundant `End Class` statements.  
  
-   Move the `End Class` statement to the appropriate location in your code.  
  
## See Also  
 [End <keyword\> Statement](../vs140/End--keyword--Statement--Visual-Basic-.md)