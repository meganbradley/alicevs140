---
title: "CMDIFrameWndEx::GetToolbarButtonToolTipText"
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
ms.assetid: f1c59fe3-db76-4200-92b1-8221cc67e445
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIFrameWndEx::GetToolbarButtonToolTipText
Called by the framework when the application displays the tooltip for a toolbar button.  
  
## Syntax  
  
```  
virtual BOOL GetToolbarButtonToolTipText(  
    CMFCToolBarButton* pButton,  
    CString& strTTText  
);  
```  
  
#### Parameters  
 [in] `pButton`  
 A pointer to a toolbar button.  
  
 [in] `strTTText`  
 The tooltip text to display for the button.  
  
## Return Value  
 `TRUE` if the tooltip has been displayed. `FALSE` otherwise.  
  
## Remarks  
  
## Requirements  
 **Header:** afxmdiframewndex.h  
  
## See Also  
 [CMDIFrameWndEx Class](../vs140/CMDIFrameWndEx-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)