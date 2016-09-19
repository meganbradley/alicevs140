---
title: "CDialogBar::Create"
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
ms.assetid: e29d21ba-72f9-4e79-b6b3-4b2f7597bbb3
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDialogBar::Create
Loads the dialog-box resource template specified by `lpszTemplateName` or `nIDTemplate`, creates the dialog-bar window, sets its style, and associates it with the `CDialogBar` object.  
  
## Syntax  
  
```  
  
      virtual BOOL Create(  
   CWnd* pParentWnd,  
   LPCTSTR lpszTemplateName,  
   UINT nStyle,  
   UINT nID   
);  
virtual BOOL Create(  
   CWnd* pParentWnd,  
   UINT nIDTemplate,  
   UINT nStyle,  
   UINT nID   
);  
```  
  
#### Parameters  
 `pParentWnd`  
 A pointer to the parent `CWnd` object.  
  
 `lpszTemplateName`  
 A pointer to the name of the `CDialogBar` object's dialog-box resource template.  
  
 `nStyle`  
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
 The control ID of the dialog bar.  
  
 `nIDTemplate`  
 The resource ID of the `CDialogBar` object's dialog-box template.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 If you specify the `CBRS_TOP` or `CBRS_BOTTOM` alignment style, the dialog bar's width is that of the frame window and its height is that of the resource specified by `nIDTemplate`. If you specify the `CBRS_LEFT` or `CBRS_RIGHT` alignment style, the dialog bar's height is that of the frame window and its width is that of the resource specified by `nIDTemplate`.  
  
## Example  
 [!CODE [NVC_MFCMessageMaps#13](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCMessageMaps#13)]  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CDialogBar Class](../vs140/CDialogBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDialogBar::CDialogBar](../vs140/CDialogBar--CDialogBar.md)