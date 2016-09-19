---
title: "CMDIChildWndEx::OnTaskbarTabThumbnailStretch"
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
ms.assetid: 670e29ef-9c14-4f30-bff0-59ccc41a1c91
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIChildWndEx::OnTaskbarTabThumbnailStretch
Called by the framework when it needs to stretch a bitmap for a Windows 7 taskbar tab thumbnail preview of the MDI child.  
  
## Syntax  
  
```  
virtual BOOL OnTaskbarTabThumbnailStretch(  
   HBITMAP hBmpDst,  
   const CRect& rectDst,  
   HBITMAP hBmpSrc,  
   const CRect& rectSrc  
);  
```  
  
#### Parameters  
 `hBmpDst`  
 A handle to a destination bitmap.  
  
 `rectDst`  
 Specifies the destination rectangle.  
  
 `hBmpSrc`  
 A handle to a source bitmap.  
  
 `rectSrc`  
 Specifies the source rectangle.  
  
## Remarks  
 Requirementher or him him him him him him him **:** afxmdichildwndex.h  
  
## See Also  
 [CMDIChildWndEx Class](../vs140/CMDIChildWndEx-Class.md)