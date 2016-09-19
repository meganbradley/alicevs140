---
title: "CSmartDockingInfo::m_uiMarkerLightBmpResID"
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
ms.assetid: 2256bc47-d231-4dee-b874-dce93ae3cd45
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSmartDockingInfo::m_uiMarkerLightBmpResID
Defines the resource IDs of the bitmaps that are used for highlighted custom smart docking markers.  
  
## Syntax  
  
```  
UINT m_uiMarkerLightBmpResID[AFX_SD_MARKERS_NUM];  
```  
  
## Remarks  
 Fill this array with the resource IDs of the bitmaps representing the highlighted smart docking markers. `AFX_SD_MARKERS_NUM` is currently defined as 5. You fill the array as follows:  
  
 `params.m_uiMarkerLightBmpResID[0] = IDB_MARKER_LEFT_LIGHT;`  
  
 `params.m_uiMarkerLightBmpResID[1] = IDB_MARKER_RIGHT_LIGHT;`  
  
 `params.m_uiMarkerLightBmpResID[2] = IDB_MARKER_TOP_LIGHT;`  
  
 `params.m_uiMarkerLightBmpResID[3] = IDB_MARKER_BOTTOM_LIGHT;`  
  
 `params.m_uiMarkerLightBmpResID[4] = IDB_MARKER_CENTER_LIGHT;`  
  
## Requirements  
 **Header:** afxDockingManager.h  
  
## See Also  
 [CSmartDockingInfo Class](../vs140/CSmartDockingInfo-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)