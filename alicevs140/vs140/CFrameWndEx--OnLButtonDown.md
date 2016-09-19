---
title: "CFrameWndEx::OnLButtonDown"
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
ms.assetid: 04dae65e-0ff3-4684-ae98-53daf2585268
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFrameWndEx::OnLButtonDown
The framework calls this method when the user presses the left mouse button.  
  
## Syntax  
  
```  
afx_msg void OnLButtonDown(  
   UINT nFlags,  
   CPoint point  
);  
```  
  
#### Parameters  
 [in] `nFlags`  
 Indicates whether the user pressed modifier keys. For possible values see the parameter `wParam` in [WM_LBUTTONDOWN Notification](http://msdn.microsoft.com/library/windows/desktop/ms645607).  
  
 [in] `point`  
 Specifies the x and y coordinates of the pointer, relative to the upper-left corner of the window.  
  
## Remarks  
  
## Requirements  
 **Header:** afxframewndex.h  
  
## See Also  
 [CFrameWndEx Class](../vs140/CFrameWndEx-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)