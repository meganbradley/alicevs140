---
title: "CBasePane::InsertPane"
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
ms.assetid: f91459d4-dab0-44a5-b6a3-23e56f644332
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBasePane::InsertPane
Registers the specified pane with the docking manager.  
  
## Syntax  
  
```  
BOOL InsertPane(  
   CBasePane* pControlBar,  
   CBasePane* pTarget,  
   BOOL bAfter = TRUE  
);  
```  
  
#### Parameters  
 [in] `pControlBar`  
 A pointer to the pane to insert.  
  
 [in] `pTarget`  
 A pointer to the adjacent pane.  
  
 [in] `bAfter`  
 If `TRUE`, `pControlBar` is inserted after `pTarget`. If `FALSE`, `pControlBar` is inserted before `pTarget`.  
  
## Return Value  
 `TRUE` if the method succeeds, `FALSE` otherwise.  
  
## Requirements  
 **Header:** afxbasepane.h  
  
## See Also  
 [CBasePane Class](../vs140/CBasePane-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)