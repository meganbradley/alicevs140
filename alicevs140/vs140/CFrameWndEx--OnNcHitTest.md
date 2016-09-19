---
title: "CFrameWndEx::OnNcHitTest"
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
ms.assetid: ec3a2105-0dfb-4f7b-88f1-258f1bd764ab
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFrameWndEx::OnNcHitTest
Called by the framework when the pointer moves or when a mouse button is pressed or released.  
  
## Syntax  
  
```  
afx_msg LRESULT OnNcHitTest(  
   CPoint point  
);  
```  
  
#### Parameters  
 [in] `point`  
 The location of the pointer in screen coordinates.  
  
## Return Value  
 A pointer hit enumerated value. For a list of possible values see [WM_NCHITTEST Notification](http://msdn.microsoft.com/library/windows/desktop/ms645618).  
  
## Remarks  
  
## Requirements  
 **Header:** afxframewndex.h  
  
## See Also  
 [CFrameWndEx Class](../vs140/CFrameWndEx-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)