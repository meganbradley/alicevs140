---
title: "CMFCToolBar::SetRouteCommandsViaFrame"
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
ms.assetid: 62a8a2d1-8046-4395-aacd-171e71df76eb
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::SetRouteCommandsViaFrame
Specifies whether the parent frame or the owner sends commands to the toolbar.  
  
## Syntax  
  
```  
void SetRouteCommandsViaFrame(  
   BOOL bValue   
);  
```  
  
#### Parameters  
 [in] `bValue`  
 If this parameter is `TRUE`, the parent frame sends commands to the toolbar. Otherwise, the owner sends commands to the toolbar.  
  
## Remarks  
 By default, the parent frame sends commands to the toolbar. Call the [CMFCToolBar::GetRouteCommandsViaFrame](../vs140/CMFCToolBar--GetRouteCommandsViaFrame.md) method to determine whether the parent frame or the owner sends commands to the toolbar.  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBar::GetRouteCommandsViaFrame](../vs140/CMFCToolBar--GetRouteCommandsViaFrame.md)