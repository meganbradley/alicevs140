---
title: "CMDIChildWndEx::OnGetIconicThumbnail"
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
ms.assetid: 0e5cdb32-1dbc-4fa1-9cc8-155e12a32673
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIChildWndEx::OnGetIconicThumbnail
Called by the framework when it needs to obtain a bitmap for the iconic thumbnail of the MDI child.  
  
## Syntax  
  
```  
virtual HBITMAP OnGetIconicThumbnail(  
   int nWidth,  
   int nHeight  
);  
```  
  
#### Parameters  
 `nWidth`  
 Specifies the width of the required bitmap.  
  
 `nHeight`  
 Specifies the height of the required bitmap.  
  
## Remarks  
  
## Requirements  
 **Header:** afxmdichildwndex.h  
  
## See Also  
 [CMDIChildWndEx Class](../vs140/CMDIChildWndEx-Class.md)