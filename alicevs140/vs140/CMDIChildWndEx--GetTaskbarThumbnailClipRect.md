---
title: "CMDIChildWndEx::GetTaskbarThumbnailClipRect"
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
ms.assetid: b3afec21-c451-4999-8795-8e96790a90e8
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIChildWndEx::GetTaskbarThumbnailClipRect
Called by the framework when it needs to select a portion of a window's client area to display as that window's thumbnail in the taskbar.  
  
## Syntax  
  
```  
virtual CRect GetTaskbarThumbnailClipRect() const;  
```  
  
## Return Value  
 A rectangle in windows coordinates. This rectangle is mapped to the client area of the top level frame. The rectangle should be empty to clear the clipping rectangle.  
  
## Remarks  
  
## Requirements  
 **Header:** afxmdichildwndex.h  
  
## See Also  
 [CMDIChildWndEx Class](../vs140/CMDIChildWndEx-Class.md)