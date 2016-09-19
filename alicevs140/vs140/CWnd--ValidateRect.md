---
title: "CWnd::ValidateRect"
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
ms.assetid: 0d35b204-1d3f-4033-9415-c952c824e547
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::ValidateRect
Validates the client area within the given rectangle by removing the rectangle from the update region of the window.  
  
## Syntax  
  
```  
  
      void ValidateRect(  
   LPCRECT lpRect   
);  
```  
  
#### Parameters  
 `lpRect`  
 Points to a [CRect](../vs140/CRect-Class.md) object or [RECT](../vs140/RECT-Structure.md) structure that contains client coordinates of the rectangle to be removed from the update region. If `lpRect` is **NULL**, the entire window is validated.  
  
## Remarks  
 The [BeginPaint](../vs140/CWnd--BeginPaint.md) member function automatically validates the entire client area. Neither the `ValidateRect` nor the [ValidateRgn](../vs140/CWnd--ValidateRgn.md) member function should be called if a portion of the update region needs to be validated before [WM_PAINT](http://msdn.microsoft.com/library/windows/desktop/dd145213) is next generated.  
  
 Windows continues to generate `WM_PAINT` messages until the current update region is validated.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::BeginPaint](../vs140/CWnd--BeginPaint.md)   
 [ValidateRect](http://msdn.microsoft.com/library/windows/desktop/dd145194)   
 [CWnd::ValidateRgn](../vs140/CWnd--ValidateRgn.md)