---
title: "CBaseTabbedPane::SetAutoDestroy"
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
ms.assetid: dc66d4fa-54b8-4a95-986d-cfc707fae244
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBaseTabbedPane::SetAutoDestroy
Determines whether the tabbed control bar will be destroyed automatically.  
  
## Syntax  
  
```  
void SetAutoDestroy(  
    BOOL bAutoDestroy = TRUE  
);  
```  
  
#### Parameters  
 [in] `bAutoDestroy`  
 `TRUE` if the tabbed pane was created dynamically and you are not controlling its lifetime; otherwise, `FALSE`.  
  
## Remarks  
 Set the auto-destroy mode to `TRUE` if you create a tabbed pane dynamically and if you are not controlling its lifetime. If auto-destroy mode is `TRUE`, the tabbed pane will be destroyed automatically by the framework.  
  
## Requirements  
 **Header:** afxBaseTabbedPane.h  
  
## See Also  
 [CBaseTabbedPane Class](../vs140/CBaseTabbedPane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)