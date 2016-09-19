---
title: "CFrameWndEx::OnSizing"
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
ms.assetid: cb5064d2-37dd-4b73-bcfe-d82e7a5251c6
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFrameWndEx::OnSizing
Called by the framework when the user resizes the frame.  
  
## Syntax  
  
```  
afx_msg void OnSizing(  
   UINT fwSide,  
   LPRECT pRect  
);  
```  
  
#### Parameters  
 [in] `fwSide`  
 The edge of the frame that is moved. See the parameter `wParam` in [WM_SIZING Notification](http://msdn.microsoft.com/library/windows/desktop/ms632647).  
  
 [in, out] `pRect`  
 Pointer to a [CRect](../vs140/CRect-Class.md) or [RECT](../vs140/RECT-Structure.md) structure that contains the frame's coordinates.  
  
## Remarks  
  
## Requirements  
 **Header:** afxframewndex.h  
  
## See Also  
 [CFrameWndEx Class](../vs140/CFrameWndEx-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)