---
title: "CMFCVisualManager::OnDrawBrowseButton"
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
ms.assetid: 881aca78-2b34-46ea-b5fe-4c3ae2aa0328
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManager::OnDrawBrowseButton
The framework calls this method when it draws the browse button for an edit control.  
  
## Syntax  
  
```  
virtual BOOL OnDrawBrowseButton(  
   CDC* pDC,  
   CRect rect,  
   CMFCEditBrowseCtrl* pEdit,  
   CMFCVisualManager::AFX_BUTTON_STATE state,  
   COLORREF& clrText   
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context.  
  
 [in] `rect`  
 A rectangle that specifies the boundary for the browse button.  
  
 [in] `pEdit`  
 A pointer to an edit control. The visual manager draws the browse button for this edit control.  
  
 [in] `state`  
 An enumerated value that specifies the state of the button.  
  
 [out] `clrText`  
 A reference to a [COLORREF](http://msdn.microsoft.com/library/windows/desktop/dd183449) parameter. This is a reserved value and is currently unused.  
  
## Return Value  
 `TRUE` if successful; otherwise `FALSE`.  
  
## Remarks  
 Override this function in a derived class if you want to customize the appearance of browse buttons in instances of the [CMFCEditBrowseCtrl Class](../vs140/CMFCEditBrowseCtrl-Class.md). The possible values for the state of the button are `ButtonsIsRegular`, `ButtonsIsPressed`, and `ButtonsIsHighlighted`.  
  
## Requirements  
 **Header:** afxvisualmanager.h  
  
## See Also  
 [CMFCVisualManager Class](../vs140/CMFCVisualManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCEditBrowseCtrl Class](../vs140/CMFCEditBrowseCtrl-Class.md)