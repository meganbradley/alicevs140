---
title: "CAtlPreviewCtrlImpl::SetPreviewVisuals"
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
ms.assetid: 2acc2023-d399-4703-83d2-f2a099fb6101
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlPreviewCtrlImpl::SetPreviewVisuals
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
 Background color of the preview window.  
  
 `clrText`  
 Text color of the preview window.  
  
 `plf`  
 Font used to display text in the preview window.  
  
## Remarks  
  
## Requirements  
 **Header:** atlpreviewctrlimpl.h  
  
## See Also  
 [CAtlPreviewCtrlImpl Class](../vs140/CAtlPreviewCtrlImpl-Class.md)