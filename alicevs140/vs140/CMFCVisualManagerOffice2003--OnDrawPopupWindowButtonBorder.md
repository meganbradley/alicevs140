---
title: "CMFCVisualManagerOffice2003::OnDrawPopupWindowButtonBorder"
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
ms.assetid: f143dca9-891f-483e-a495-2be4ad5930bd
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManagerOffice2003::OnDrawPopupWindowButtonBorder
The framework calls this method when it draws the border of button in a popup window.  
  
## Syntax  
  
```  
virtual void OnDrawPopupWindowButtonBorder(  
   CDC* pDC,  
   CRect rectClient,  
   CMFCDesktopAlertWndButton* pButton  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 Pointer to the device context of the button.  
  
 [in] `rectClient`  
 Bounding rectangle of the button.  
  
 [in] `pButton`  
 Pointer to the button (a [CMFCDesktopAlertWndButton](../vs140/CMFCDesktopAlertWndButton-Class.md) object).  
  
## Remarks  
  
## Requirements  
 **Header:** afxvisualmanageroffice2003.h  
  
## See Also  
 [CMFCVisualManagerOffice2003 Class](../vs140/CMFCVisualManagerOffice2003-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)