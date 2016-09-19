---
title: "CRectTracker::SetCursor"
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
ms.assetid: ebe5425a-17dc-4089-870c-79b394cae894
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRectTracker::SetCursor
Call this function to change the cursor shape while it is over the `CRectTracker` object's region.  
  
## Syntax  
  
```  
  
      BOOL SetCursor(  
   CWnd* pWnd,  
   UINT nHitTest   
) const;  
```  
  
#### Parameters  
 `pWnd`  
 Points to the window that currently contains the cursor.  
  
 `nHitTest`  
 Results of the previous hit test, from the `WM_SETCURSOR` message.  
  
## Return Value  
 Nonzero if the previous hit was over the tracker rectangle; otherwise 0.  
  
## Remarks  
 Call this function from inside the function of your window that handles the `WM_SETCURSOR` message (typically `OnSetCursor`).  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CRectTracker Class](../vs140/CRectTracker-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRectTracker::NormalizeHit](../vs140/CRectTracker--NormalizeHit.md)   
 [CRectTracker::HitTest](../vs140/CRectTracker--HitTest.md)   
 [CWinApp::LoadCursor](../vs140/CWinApp--LoadCursor.md)   
 [CWnd::OnSetCursor](../vs140/CWnd--OnSetCursor.md)