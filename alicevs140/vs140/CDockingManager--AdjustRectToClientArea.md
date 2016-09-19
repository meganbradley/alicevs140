---
title: "CDockingManager::AdjustRectToClientArea"
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
ms.assetid: 590c51a6-3a6c-4b75-9ca7-d8228b44b042
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDockingManager::AdjustRectToClientArea
Adjusts the alignment of a rectangle.  
  
## Syntax  
  
```  
virtual BOOL AdjustRectToClientArea(  
   CRect& rectResult,  
   DWORD dwAlignment  
);  
```  
  
#### Parameters  
 [in] `rectResult`  
 A reference to a `CRect` object  
  
 [in] `dwAlignment`  
 The alignment of the `CRect` object  
  
## Return Value  
 `TRUE` if the alignment of the `CRect` object was adjusted; `FALSE` otherwise.  
  
## Remarks  
 The `dwAlignment` parameter can have one of the following values:  
  
-   CBRS_ALIGN_TOP  
  
-   CBRS_ALIGN_BOTTOM  
  
-   CBRS_ALIGN_LEFT  
  
-   CBRS_ALIGN_RIGHT  
  
## Requirements  
 **Header:** afxdockingmanager.h  
  
## See Also  
 [CDockingManager Class](../vs140/CDockingManager-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)