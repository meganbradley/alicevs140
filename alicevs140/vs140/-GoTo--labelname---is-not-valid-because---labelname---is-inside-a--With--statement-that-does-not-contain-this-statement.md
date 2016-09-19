---
title: "&#39;GoTo &lt;labelname&gt;&#39; is not valid because &#39;&lt;labelname&gt;&#39; is inside a &#39;With&#39; statement that does not contain this statement"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9c39d4ad-0b9b-45e9-b6c2-d983144b5b23
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;GoTo &lt;labelname&gt;&#39; is not valid because &#39;&lt;labelname&gt;&#39; is inside a &#39;With&#39; statement that does not contain this statement
`GoTo` statements are restricted to jumps within the current block of code.  
  
 **Error ID:** BC30756  
  
### To correct this error  
  
-   Restructure your code so that the `GoTo` statement and the label are both inside the `With` block.  
  
## See Also  
 [GoTo Statement](../vs140/GoTo-Statement.md)