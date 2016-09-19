---
title: "CBasePane::GetRecentVisibleState"
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
ms.assetid: e6f81336-dd06-4352-aacf-d948b21a413d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBasePane::GetRecentVisibleState
The framework calls this method when a pane is restored from an archive.  
  
## Syntax  
  
```  
virtual BOOL GetRecentVisibleState() const;  
```  
  
## Return Value  
 A `BOOL` that specifies the recent visible state. If `TRUE`, the pane was visible when serialized and should be visible when restored. If `FALSE`, the pane was hidden when serialized and should be hidden when restored.  
  
## Requirements  
 **Header:** afxbasepane.h  
  
## See Also  
 [CBasePane Class](../vs140/CBasePane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)