---
title: "CFindReplaceDialog::ReplaceAll"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: d8c4a37a-f712-4d53-88ee-d658a95524ea
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFindReplaceDialog::ReplaceAll
Call this function to determine whether the user wants all occurrences of the string to be replaced.  
  
## Syntax  
  
```  
  
BOOL ReplaceAll( ) const;  
```  
  
## Return Value  
 Nonzero if the user has requested that all strings matching the replace string be replaced; otherwise 0.  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CFindReplaceDialog Class](../vs140/CFindReplaceDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFindReplaceDialog::ReplaceCurrent](../vs140/CFindReplaceDialog--ReplaceCurrent.md)