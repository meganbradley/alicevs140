---
title: "CDocument::m_bGetThumbnailMode"
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
ms.assetid: da4985a7-338f-4e01-a4d5-e367779dfb74
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDocument::m_bGetThumbnailMode
Specifies that the `CDocument` object was created by dllhost for thumbnails. Should be checked in `CView::OnDraw`.  
  
## Syntax  
  
```  
BOOL m_bGetThumbnailMode;  
```  
  
## Remarks  
 `TRUE` indicates that the document was created by dllhost for thumbnails.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDocument Class](../vs140/CDocument-Class.md)