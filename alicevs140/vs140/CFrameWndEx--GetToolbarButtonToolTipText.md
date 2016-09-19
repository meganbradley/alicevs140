---
title: "CFrameWndEx::GetToolbarButtonToolTipText"
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
ms.assetid: 44eb7c97-9d39-48b2-930e-e7d32a120035
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFrameWndEx::GetToolbarButtonToolTipText
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
 By default, this method does nothing. Override this method if you want to display the tooltip for the toolbar button.  
  
## Requirements  
 **Header:** afxframewndex.h  
  
## See Also  
 [CFrameWndEx Class](../vs140/CFrameWndEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)