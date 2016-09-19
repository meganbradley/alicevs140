---
title: "CFindReplaceDialog::ReplaceCurrent"
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
ms.assetid: fb368db0-cba7-424a-8308-9c9848fd11e5
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFindReplaceDialog::ReplaceCurrent
Call this function to determine whether the user wants the current word to be replaced.  
  
## Syntax  
  
```  
  
BOOL ReplaceCurrent( ) const;  
```  
  
## Return Value  
 Nonzero if the user has requested that the currently selected string be replaced with the replace string; otherwise 0.  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CFindReplaceDialog Class](../vs140/CFindReplaceDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFindReplaceDialog::ReplaceAll](../vs140/CFindReplaceDialog--ReplaceAll.md)