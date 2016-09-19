---
title: "CPaneFrameWnd::FrameFromPoint"
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
ms.assetid: a9ac4bac-0168-4d08-99ae-3e7c925b86ff
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPaneFrameWnd::FrameFromPoint
Finds the mini-frame window that contains the specified point.  
  
## Syntax  
  
```  
static CPaneFrameWnd* __stdcall FrameFromPoint(  
   CPoint pt,  
   int nSensitivity,  
   CPaneFrameWnd* pFrameToExclude = NULL,  
   BOOL bFloatMultiOnly = FALSE  
);  
```  
  
#### Parameters  
 [in] `pt`  
 The point, in screen coordinates.  
  
 [in] `nSensitivity`  
 Increase the search area of the mini-frame window by this size. A mini-frame window satisfies the search criteria if the given point falls in the increased area.  
  
 [in] `pFrameToExclude`  
 Specifies a mini-frame window to exclude from the search.  
  
 [in] `bFloatMultiOnly`  
 If `TRUE`, only search mini-frame windows that have the `CBRS_FLOAT_MULTI` style. If `FALSE`, search all mini-frame windows.  
  
## Return Value  
 A pointer to the mini-frame window that contains `pt`; otherwise `NULL`.  
  
## Requirements  
 **Header:** afxpaneframewnd.h  
  
## See Also  
 [CPaneFrameWnd Class](../vs140/CPaneFrameWnd-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)