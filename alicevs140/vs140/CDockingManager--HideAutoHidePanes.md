---
title: "CDockingManager::HideAutoHidePanes"
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
ms.assetid: 83a62ee1-3a08-4b53-a228-edf1eedb9b8e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDockingManager::HideAutoHidePanes
Hides a pane that is in autohide mode.  
  
## Syntax  
  
```  
void HideAutoHidePanes(  
   CDockablePane* pBarToExclude = NULL,  
   BOOL bImmediately = FALSE  
);  
```  
  
#### Parameters  
 [in] `pBarToExclude`  
 A pointer to a bar to exclude from hiding.  
  
 [in] `bImmediately`  
 `TRUE` to hide the pane immediately; `FALSE` to hide the pane with the autohide effect.  
  
## Requirements  
 **Header:** afxdockingmanager.h  
  
## See Also  
 [CDockingManager Class](../vs140/CDockingManager-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)