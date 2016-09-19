---
title: "CWnd::GetDCRenderTarget"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: 3d50fa45-a69c-4db4-aea5-ba86f8f39a70
caps.latest.revision: 7
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::GetDCRenderTarget
Retrieves the device context (DC) render target for the `CWnd` window.  
  
## Syntax  
  
```  
  
CDCRenderTarget* GetDCRenderTarget();  
  
```  
  
## Return Value  
 The device context render target for the specified window if the function is successful; otherwise **NULL**.  
  
## Remarks  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::BeginPaint](../vs140/CWnd--BeginPaint.md)   
 [CWnd::GetDC](../vs140/CWnd--GetDC.md)   
 [CWnd::GetWindowDC](../vs140/CWnd--GetWindowDC.md)   
 [CWnd::ReleaseDC](../vs140/CWnd--ReleaseDC.md)   
 [GetDCEx](http://msdn.microsoft.com/library/windows/desktop/dd144873)