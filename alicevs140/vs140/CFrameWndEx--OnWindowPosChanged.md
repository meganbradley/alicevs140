---
title: "CFrameWndEx::OnWindowPosChanged"
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
ms.assetid: c413dda3-fbad-4de2-8c88-39ccba50ec11
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFrameWndEx::OnWindowPosChanged
Called by the framework when the frame size, position, or z-order has changed because of a call to a window management method.  
  
## Syntax  
  
```  
afx_msg void OnWindowPosChanged(  
   WINDOWPOS FAR* lpwndpos  
);  
```  
  
#### Parameters  
 [in] `lpwndpos`  
 Pointer to a [WINDOWPOS](../vs140/WINDOWPOS-Structure.md) structure that contains the new size and position.  
  
## Remarks  
  
## Requirements  
 **Header:** afxframewndex.h  
  
## See Also  
 [CFrameWndEx Class](../vs140/CFrameWndEx-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)