---
title: "CMFCPreviewCtrlImpl::SetPreviewVisuals"
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
ms.assetid: c2a3f709-d71a-4ee4-a918-b602f0f3ba03
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPreviewCtrlImpl::SetPreviewVisuals
Called by a Rich Preview handler when it needs to set visuals of rich preview content.  
  
## Syntax  
  
```  
virtual void SetPreviewVisuals(  
   COLORREF clrBack,  
   COLORREF clrText,  
   const LOGFONTW *plf  
);  
```  
  
#### Parameters  
 `clrBack`  
 Background color of preview window.  
  
 `clrText`  
 Text color of preview window.  
  
 `plf`  
 Font used to display text in the preview window.  
  
## Remarks  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CMFCPreviewCtrlImpl Class](../vs140/CMFCPreviewCtrlImpl-Class.md)