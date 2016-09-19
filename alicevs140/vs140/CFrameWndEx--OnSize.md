---
title: "CFrameWndEx::OnSize"
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
ms.assetid: c36d08b8-0223-40f3-a863-fc18ff3e26c3
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFrameWndEx::OnSize
Called by the framework after the frame's size changes.  
  
## Syntax  
  
```  
afx_msg void OnSize(  
   UINT nType,  
   int cx,  
   int cy  
);  
```  
  
#### Parameters  
 [in] `nType`  
 The type of resizing. For possible values see the parameter `wParam` in [WM_SIZE Notification](http://msdn.microsoft.com/library/windows/desktop/ms632646).  
  
 [in] `cx`  
 New width of the frame in pixels.  
  
 [in] `cy`  
 New height of the frame in pixels.  
  
## Remarks  
  
## Requirements  
 **Header:** afxframewndex.h  
  
## See Also  
 [CFrameWndEx Class](../vs140/CFrameWndEx-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)