---
title: "CToolBar::Create"
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
ms.assetid: b2d46cc4-38ab-47bf-b0a2-840e2eb736e2
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolBar::Create
This member function creates a Windows toolbar (a child window) and associates it with the `CToolBar` object.  
  
## Syntax  
  
```  
  
      virtual BOOL Create(  
   CWnd* pParentWnd,  
   DWORD dwStyle = WS_CHILD |  WS_VISIBLE | CBRS_TOP,  
   UINT nID = AFX_IDW_TOOLBAR   
);  
```  
  
#### Parameters  
 `pParentWnd`  
 Pointer to the window that is the toolbar's parent.  
  
 `dwStyle`  
 The toolbar style. Additional toolbar styles supported are:  
  
-   `CBRS_TOP` Control bar is at top of the frame window.  
  
-   `CBRS_BOTTOM` Control bar is at bottom of the frame window.  
  
-   `CBRS_NOALIGN` Control bar is not repositioned when the parent is resized.  
  
-   `CBRS_TOOLTIPS` Control bar displays tool tips.  
  
-   **CBRS_SIZE_DYNAMIC** Control bar is dynamic.  
  
-   **CBRS_SIZE_FIXED** Control bar is fixed.  
  
-   **CBRS_FLOATING** Control bar is floating.  
  
-   `CBRS_FLYBY` Status bar displays information about the button.  
  
-   **CBRS_HIDE_INPLACE** Control bar is not displayed to the user.  
  
 `nID`  
 The toolbar's child-window ID.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 It also sets the toolbar height to a default value.  
  
## Example  
 [!CODE [NVC_MFCDocView#179](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#179)]  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CToolBar Class](../vs140/CToolBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CToolBar::CToolBar](../vs140/CToolBar--CToolBar.md)   
 [CToolBar::LoadBitmap](../vs140/CToolBar--LoadBitmap.md)   
 [CToolBar::SetButtons](../vs140/CToolBar--SetButtons.md)   
 [CToolBar::LoadToolBar](../vs140/CToolBar--LoadToolBar.md)   
 [CControlBar::CalcDynamicLayout](../vs140/CControlBar--CalcDynamicLayout.md)   
 [CControlBar::CalcFixedLayout](../vs140/CControlBar--CalcFixedLayout.md)