---
title: "CMDIChildWndEx::SetTaskbarThumbnailClipRect"
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
ms.assetid: 1c66dedd-ead4-4496-bdb3-88faa1610d79
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIChildWndEx::SetTaskbarThumbnailClipRect
Called by the framework to set the clipping rectangle to select a portion of a window's client area to display as that window's thumbnail in the taskbar.  
  
## Syntax  
  
```  
virtual BOOL SetTaskbarThumbnailClipRect(  
   CRect rect  
);  
```  
  
#### Parameters  
 `rect`  
 Specifies the new clipping rectangle. If the rectangle is empty or null, the clipping is removed.  
  
## Return Value  
 `TRUE` if successful; otherwise `FALSE`.  
  
## Remarks  
  
## Requirements  
 **Header:** afxmdichildwndex.h  
  
## See Also  
 [CMDIChildWndEx Class](../vs140/CMDIChildWndEx-Class.md)