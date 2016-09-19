---
title: "CMFCPreviewCtrlImpl::SetRect"
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
ms.assetid: a251dc51-ec36-4b50-a373-b02b2b1e73eb
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPreviewCtrlImpl::SetRect
Sets a new bounding rectangle for this control.  
  
## Syntax  
  
```  
virtual void SetRect(  
   const RECT* prc,  
   BOOL bRedraw  
);  
```  
  
#### Parameters  
 `prc`  
 Specifies the new size and position of the preview control.  
  
 `bRedraw`  
 Specifies whether the control should be redrawn.  
  
## Remarks  
 Usually a new bounding rectangle is set when the host control is resized.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CMFCPreviewCtrlImpl Class](../vs140/CMFCPreviewCtrlImpl-Class.md)