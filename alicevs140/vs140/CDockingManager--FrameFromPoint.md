---
title: "CDockingManager::FrameFromPoint"
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
ms.assetid: 7248419f-f41c-420f-8e4e-bdc40d7ac10d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDockingManager::FrameFromPoint
Returns the frame that contains the given point.  
  
## Syntax  
  
```  
virtual CPaneFrameWnd* FrameFromPoint(  
   CPoint pt,  
   CPaneFrameWnd* pFrameToExclude,  
   BOOL bFloatMultiOnly  
) const;  
```  
  
#### Parameters  
 [in] `pt`  
 Specifies the point, in screen coordinates, to check.  
  
 [in] `pFrameToExclude`  
 A pointer to a frame to exclude.  
  
 [in] `bFloatMultiOnly`  
 `TRUE` to exclude frames that are not instances of `CMultiPaneFrameWnd`; `FALSE` otherwise.  
  
## Return Value  
 The frame that contains the given point; `NULL` otherwise.  
  
## Requirements  
 **Header:** afxdockingmanager.h  
  
## See Also  
 [CDockingManager Class](../vs140/CDockingManager-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)