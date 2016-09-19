---
title: "&#39;Option Compare&#39; must be followed by &#39;Text&#39; or &#39;Binary&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e59cf10d-47ce-401d-8474-3b69a3a5f5db
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;Option Compare&#39; must be followed by &#39;Text&#39; or &#39;Binary&#39;
An `Option Compare` statement contains an incorrect setting or no setting. The only settings allowed in `Option Compare` are `Text` and `Binary`.  
  
 **Error ID:** BC30207  
  
### To correct this error  
  
1.  Check to see if the setting specifier is misspelled.  
  
2.  Add either `Text` or `Binary` to the `Option Compare` statement; for example, `Option Compare Text`.  
  
## See Also  
 [Option Compare Statement](../Topic/Option%20Compare%20Statement.md)