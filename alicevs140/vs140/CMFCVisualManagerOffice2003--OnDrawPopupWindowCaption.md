---
title: "CMFCVisualManagerOffice2003::OnDrawPopupWindowCaption"
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
ms.assetid: 2489343a-bad3-4da7-a8d6-4256f6a7ede0
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManagerOffice2003::OnDrawPopupWindowCaption
The framework calls this method when it draws the caption of a popup window.  
  
## Syntax  
  
```  
virtual COLORREF OnDrawPopupWindowCaption(  
   CDC* pDC,  
   CRect rectCaption,  
   CMFCDesktopAlertWnd* pPopupWnd  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 Pointer to the device context of the caption.  
  
 [in] `rectCaption`  
 Bounding rectangle of the caption.  
  
 [in] `pPopupWnd`  
 Pointer to the popup window for which the caption is to be drawn.  
  
## Return Value  
 The text color of the caption.  
  
## Remarks  
 Override this method in a derived visual manager to customize the appearance of popup-window captions.  
  
## Requirements  
 **Header:** afxvisualmanageroffice2003.h  
  
## See Also  
 [CMFCVisualManagerOffice2003 Class](../vs140/CMFCVisualManagerOffice2003-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)