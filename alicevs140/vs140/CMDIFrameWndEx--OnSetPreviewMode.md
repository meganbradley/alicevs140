---
title: "CMDIFrameWndEx::OnSetPreviewMode"
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
ms.assetid: a599ac4b-fa71-4a55-8ca4-8c8c98b96284
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIFrameWndEx::OnSetPreviewMode
Sets the application's main frame window print-preview mode.  
  
## Syntax  
  
```  
virtual void OnSetPreviewMode(  
   BOOL bPreview,  
   CPrintPreviewState* pState  
);  
```  
  
#### Parameters  
 [in] `bPreview`  
 If `TRUE`, sets print-preview mode. If `FALSE`, cancels preview mode.  
  
 [in] `pState`  
 A pointer to a `CPrintPreviewState` structure.  
  
## Remarks  
 This method overrides [CFrameWnd::OnSetPreviewMode](../vs140/CFrameWnd--OnSetPreviewMode.md).  
  
## Requirements  
 **Header:** afxmdiframewndex.h  
  
## See Also  
 [CMDIFrameWndEx Class](../vs140/CMDIFrameWndEx-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)