---
title: "&#39;GoTo &lt;labelname&gt;&#39; is not valid because &#39;&lt;labelname&gt;&#39; is inside a &#39;For&#39; or &#39;For Each&#39; statement that does not contain this statement"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: be28bec5-1bc4-4da1-ba0c-4e3faac81077
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;GoTo &lt;labelname&gt;&#39; is not valid because &#39;&lt;labelname&gt;&#39; is inside a &#39;For&#39; or &#39;For Each&#39; statement that does not contain this statement
`GoTo` statements are restricted to jumps within the current block of code.  
  
 **Error ID:** BC30757  
  
### To correct this error  
  
-   Restructure your code so that the `GoTo` statement and the label are both inside the `For` block.  
  
## See Also  
 [GoTo Statement](../vs140/GoTo-Statement.md)   
 [For (Visual Basic)](assetId:///c470a263-9b49-4308-8fd6-8592b84a7980)