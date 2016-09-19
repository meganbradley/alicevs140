---
title: "CDockingManager::ReplacePane"
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
ms.assetid: c3bb78bc-fa81-472c-a136-a9db5dc0f165
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDockingManager::ReplacePane
Replaces one pane with another.  
  
## Syntax  
  
```  
BOOL ReplacePane(  
   CDockablePane* pOriginalBar,  
   CDockablePane* pNewBar  
);  
```  
  
#### Parameters  
 [in] `pOriginalBar`  
 A pointer to the original pane.  
  
 [in] `pNewBar`  
 A pointer to the pane that replaces the original pane.  
  
## Return Value  
 `TRUE` if the pane is successfully replaced; `FALSE` otherwise.  
  
## Requirements  
 **Header:** afxdockingmanager.h  
  
## See Also  
 [CDockingManager Class](../vs140/CDockingManager-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)