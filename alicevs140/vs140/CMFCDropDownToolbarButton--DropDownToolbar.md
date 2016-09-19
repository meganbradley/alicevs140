---
title: "CMFCDropDownToolbarButton::DropDownToolbar"
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
ms.assetid: 386c0c52-e92a-467a-96cb-6135f878f0b4
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCDropDownToolbarButton::DropDownToolbar
Opens a drop-down toolbar.  
  
## Syntax  
  
```  
BOOL DropDownToolbar(  
   CWnd* pWnd  
);  
```  
  
#### Parameters  
 [in] `pWnd`  
 The parent window of the drop-down frame, or `NULL` to use the parent window of the drop-down toolbar button.  
  
## Return Value  
 Nonzero if the method is successful; otherwise 0.  
  
## Remarks  
 The [CMFCDropDownToolbarButton::OnClick](../vs140/CMFCDropDownToolbarButton--OnClick.md) method calls this method to open the drop-down toolbar when the user presses and holds the toolbar button down.  
  
 This methods creates the drop-down toolbar by using the [CMFCDropDownFrame::Create](../vs140/CMFCDropDownFrame--Create.md) method. If the parent toolbar is docked vertically, this method positions the drop-down toolbar either to the left-hand or right-hand side of the parent toolbar, depending on the fit. Otherwise, this method positions the drop-down toolbar underneath the parent toolbar.  
  
 This method fails if `pWnd` is `NULL` and the drop-down toolbar button does not have a parent window.  
  
## Requirements  
 **Header:** afxdropdowntoolbar.h  
  
## See Also  
 [CMFCDropDownToolbarButton Class](../vs140/CMFCDropDownToolbarButton-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCDropDownToolbarButton::OnClick](../vs140/CMFCDropDownToolbarButton--OnClick.md)   
 [CMFCDropDownFrame::Create](../vs140/CMFCDropDownFrame--Create.md)