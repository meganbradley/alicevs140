---
title: "CMFCVisualManagerOffice2003::OnErasePopupWindowButton"
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
ms.assetid: 53237b31-6f68-434e-bbd7-0bfde4f7bf3f
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManagerOffice2003::OnErasePopupWindowButton
The framework calls this method when it erases a button in a popup window.  
  
## Syntax  
  
```  
virtual void OnErasePopupWindowButton(  
   CDC* pDC,  
   CRect rectClient,  
   CMFCDesktopAlertWndButton* pButton  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context.  
  
 [in] `rectClient`  
 The rectangle that specifies the client area of the popup window.  
  
 [in] `pButton`  
 Pointer to the button to be erased.  
  
## Remarks  
  
## Requirements  
 **Header:** afxvisualmanageroffice2003.h  
  
## See Also  
 [CMFCVisualManagerOffice2003 Class](../vs140/CMFCVisualManagerOffice2003-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)