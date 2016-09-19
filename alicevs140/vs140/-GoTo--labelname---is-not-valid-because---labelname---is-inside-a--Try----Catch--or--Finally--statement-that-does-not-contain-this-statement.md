---
title: "&#39;GoTo &lt;labelname&gt;&#39; is not valid because &#39;&lt;labelname&gt;&#39; is inside a &#39;Try&#39;, &#39;Catch&#39; or &#39;Finally&#39; statement that does not contain this statement"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2eefc7fb-fdf0-41e9-bf60-c3bc93580e14
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;GoTo &lt;labelname&gt;&#39; is not valid because &#39;&lt;labelname&gt;&#39; is inside a &#39;Try&#39;, &#39;Catch&#39; or &#39;Finally&#39; statement that does not contain this statement
You cannot branch into a `Try...Catch...Finally` block.  
  
 **Error ID:** BC30754  
  
### To correct this error  
  
-   Restructure your code so that the label precedes the `Try...Catch...Finally` block.  
  
## See Also  
 [Try...Catch...Finally Statement](../vs140/Try...Catch...Finally-Statement--Visual-Basic-.md)