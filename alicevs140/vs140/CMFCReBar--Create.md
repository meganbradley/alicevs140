---
title: "CMFCReBar::Create"
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
ms.assetid: e41d527d-c60e-4e74-950d-aab231a78f9f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCReBar::Create
Creates the rebar control and attaches it to the [CMFCReBar](../vs140/CMFCReBar-Class.md) object.  
  
## Syntax  
  
```  
BOOL Create(  
    CWnd* pParentWnd,  
    DWORD dwCtrlStyle = RBS_BANDBORDERS,  
    DWORD dwStyle = WS_CHILD | WS_VISIBLE | WS_CLIPSIBLINGS | WS_CLIPCHILDREN | CBRS_TOP,  
    UINT nID = AFX_IDW_REBAR   
);  
```  
  
#### Parameters  
 [in] [out] `pParentWnd`  
 A pointer to the parent window of this rebar control.  
  
 [in] `dwCtrlStyle`  
 Specifies the style for the rebar control. The default style value is **RBS_BANDBORDERS**, which displays narrow lines to separate adjacent bands on the rebar control. For a list of valid styles, see [Rebar Control Styles](http://msdn.microsoft.com/library/windows/desktop/bb774377) in the Windows SDK documentation.  
  
 [in] `dwStyle`  
 The window style of the rebar control. For a list of valid styles, see [Window Styles](../vs140/Window-Styles.md).  
  
 [in] `nID`  
 The rebar's child-window ID.  
  
## Return Value  
 `TRUE` if the rebar was created successfully; otherwise, `FALSE`.  
  
## Remarks  
  
## Requirements  
 **Header:** afxRebar.h  
  
## See Also  
 [CMFCReBar Class](../vs140/CMFCReBar-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)