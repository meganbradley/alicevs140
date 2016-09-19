---
title: "CPaneFrameWnd::GetCaptionHeight"
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
ms.assetid: 6d43b061-0aa7-4a57-a2a5-204e818489b8
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPaneFrameWnd::GetCaptionHeight
Returns the height of the mini-frame window caption.  
  
## Syntax  
  
```  
virtual int GetCaptionHeight() const;  
```  
  
## Return Value  
 The height, in pixels, of the mini-frame window.  
  
## Remarks  
 Call this method to determine the height of a mini-frame window. By default, the height is set to `SM_CYSMCAPTION`. For more information, see [GetSystemMetrics Function](http://msdn.microsoft.com/library/windows/desktop/ms724385).  
  
## Requirements  
 **Header:** afxPaneFrameWnd.h  
  
## See Also  
 [CPaneFrameWnd Class](../vs140/CPaneFrameWnd-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)