---
title: "CBasePane::GetParentMiniFrame"
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
ms.assetid: 518ffa89-7c6b-4415-ae13-815a082ad7d3
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBasePane::GetParentMiniFrame
Returns a pointer to the parent mini-frame window.  
  
## Syntax  
  
```  
virtual CPaneFrameWnd* GetParentMiniFrame(  
   BOOL bNoAssert=FALSE  
) const;  
```  
  
#### Parameters  
 [in] `bNoAssert`  
 If `TRUE`, this method does not check for non-valid pointers. If you call this method when your application exits, set this parameter to `TRUE`.  
  
## Return Value  
 A valid pointer to the parent mini-frame window if the pane is floating; otherwise `NULL`.  
  
## Remarks  
 Call this function to retrieve a pointer to the parent mini-frame window. This method iterates through all parents and checks for an object derived from [CPaneFrameWnd Class](../vs140/CPaneFrameWnd-Class.md).  
  
 Use `GetParentMiniFrame` to determine whether the pane is floating.  
  
## Requirements  
 **Header:** afxbasepane.h  
  
## See Also  
 [CBasePane Class](../vs140/CBasePane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)