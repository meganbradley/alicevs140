---
title: "CMFCToolBarDateTimeCtrl::OnUpdateToolTip"
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
ms.assetid: 7fdf0312-02b0-471c-8253-d91f30845bf0
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarDateTimeCtrl::OnUpdateToolTip
Called by the framework when the parent toolbar updates its tooltip text.  
  
## Syntax  
  
```  
virtual BOOL OnUpdateToolTip(  
   CWnd* pWndParent,  
   int iButtonIndex,  
   CToolTipCtrl& wndToolTip,  
   CString& str  
);  
```  
  
#### Parameters  
 [in] `pWndParent`  
 The parent window.  
  
 [in] `iButtonIndex`  
 The zero-based index of the button in the parent button collection.  
  
 [in] `wndToolTip`  
 The control that displays the tooltip text.  
  
 [out] `str`  
 A `CString` object that receives the updated tooltip text.  
  
## Return Value  
 Nonzero if the method updates the tooltip text; otherwise 0.  
  
## Remarks  
 This method extends the base class implementation ([CMFCToolBarButton::OnUpdateToolTip](../vs140/CMFCToolBarButton--OnUpdateToolTip.md)) by displaying the tooltip text that is associated with the button. If the button is not docked horizontally, this method does nothing and returns `FALSE`.  
  
## Requirements  
 **Header:** afxtoolbardatetimectrl.h  
  
## See Also  
 [CMFCToolBarDateTimeCtrl Class](../vs140/CMFCToolBarDateTimeCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBarButton::OnUpdateToolTip](../vs140/CMFCToolBarButton--OnUpdateToolTip.md)