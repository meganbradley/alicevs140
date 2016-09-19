---
title: "&#39;Exit&#39; must be followed by &#39;Sub&#39;, &#39;Function&#39;, &#39;Property&#39;, &#39;Do&#39;, &#39;For&#39;, &#39;While&#39;, &#39;Select&#39;, or &#39;Try&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 91078689-f4bf-4331-a475-10bc9fe7cd0c
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;Exit&#39; must be followed by &#39;Sub&#39;, &#39;Function&#39;, &#39;Property&#39;, &#39;Do&#39;, &#39;For&#39;, &#39;While&#39;, &#39;Select&#39;, or &#39;Try&#39;
An `Exit` statement contains an invalid keyword. `Exit` must specify the block from which control is to be transferred to the statement following the block; for example, `End While`.  
  
 **Error ID:** BC30240  
  
### To correct this error  
  
-   Add a valid keyword following `Exit`, or remove the `Exit` statement.  
  
## See Also  
 [Exit Statement](../vs140/Exit-Statement--Visual-Basic-.md)