---
title: "CMFCColorBar::GetCommandID"
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
ms.assetid: f2fc928d-c4d7-40af-8560-2f28468c0238
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCColorBar::GetCommandID
Retrieves the command ID of the current color bar control.  
  
## Syntax  
  
```  
UINT GetCommandID() const;  
```  
  
## Return Value  
 A command ID.  
  
## Remarks  
 When the user selects a new color, the framework sends the command ID in a `WM_COMMAND` message to notify the parent of the `CMFCColorBar` object.  
  
## Requirements  
 **Header:** afxcolorbar.h  
  
## See Also  
 [CMFCColorBar Class](../vs140/CMFCColorBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)