---
title: "CMDIFrameWndEx::PaneFromPoint"
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
ms.assetid: f5c3864b-d569-4ed0-9d45-bd22cc552691
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIFrameWndEx::PaneFromPoint
Returns the docking pane that contains the specified point.  
  
## Syntax  
  
```  
CBasePane* PaneFromPoint(  
   CPoint point,  
   int nSensitivity,  
   bool bExactBar,  
   CRuntimeClass* pRTCBarType   
) const;  
CBasePane* PaneFromPoint(  
   CPoint point,  
   int nSensitivity,  
   DWORD& dwAlignment,  
   CRuntimeClass* pRTCBarType   
) const;  
```  
  
#### Parameters  
 [in] `point`  
 The point (in screen coordinates).  
  
 [in] `nSensitivity`  
 The window rectangle of each checked pane is enlarged in all directions by this value.  
  
 [in] `bExactBar`  
 If `TRUE`, the `nSensitivity` parameter is ignored.  
  
 [in] `pRTCBarType`  
 If non-`NULL`, the method iterates over only the panes of the specified type.  
  
 [out] `dwAlignment`  
 If a pane is found, this parameter will specify which side of the pane is closest to the specified point.  
  
## Return Value  
 A pointer to a docking pane, or `NULL` if no control contains the point specified by `point`.  
  
## Remarks  
 The call is redirected to the [CDockingManager Class](../vs140/CDockingManager-Class.md). See [CDockingManager::PaneFromPoint](../vs140/CDockingManager--PaneFromPoint.md) for more information.  
  
## Requirements  
 **Header:** afxMDIFrameWndEx.h  
  
## See Also  
 [CMDIFrameWndEx Class](../vs140/CMDIFrameWndEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)