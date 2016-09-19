---
title: "CWnd::EnableD2DSupport"
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
ms.assetid: ba908947-5ee6-457c-b447-12c0573fbe57
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::EnableD2DSupport
Enables or disables window D2D support. Call this method before the main window is initialized.  
  
## Syntax  
  
```  
void EnableD2DSupport(  
   BOOL bEnable = TRUE,  
   BOOL bUseDCRenderTarget = FALSE  
);  
```  
  
#### Parameters  
 `bEnable`  
 Specifies whether to turn on, or off D2D support.  
  
 `bUseDCRenderTarget`  
 Species whether to use the Device Context (DC) render target, CDCRenderTarget. If FALSE, CHwndRenderTarget is used.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)