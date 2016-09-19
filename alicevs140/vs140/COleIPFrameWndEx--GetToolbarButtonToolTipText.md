---
title: "COleIPFrameWndEx::GetToolbarButtonToolTipText"
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
ms.assetid: 18c6bd81-dd72-479c-99fd-4f32921b0c19
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleIPFrameWndEx::GetToolbarButtonToolTipText
Called by the framework before the tooltip for a button is displayed.  
  
## Syntax  
  
```  
virtual BOOL GetToolbarButtonToolTipText(  
   CMFCToolBarButton* pButton,  
   CString& strTTText   
);  
```  
  
#### Parameters  
 [in] `pButton`  
 Pointer to the button.  
  
 [in] `strTTText`  
 Pointer to the tooltip text.  
  
## Return Value  
 The default implementation returns 0.  
  
## Remarks  
 Override this function to customize the display of tooltips on toolbar buttons.  
  
## Requirements  
 **Header:** afxoleipframewndex.h  
  
## See Also  
 [COleIPFrameWndEx Class](../vs140/COleIPFrameWndEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)