---
title: "CMFCToolBar::Create"
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
ms.assetid: 2998c9a3-5f27-4c1f-9bc6-4ff98d4a8b20
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::Create
Creates a `CMFCToolBar` object.  
  
## Syntax  
  
```  
virtual BOOL Create(  
   CWnd* pParentWnd,  
   DWORD dwStyle=AFX_DEFAULT_TOOLBAR_STYLE,  
   UINT nID=AFX_IDW_TOOLBAR   
);  
```  
  
#### Parameters  
 [in] `pParentWnd`  
 A pointer to the parent window of the toolbar.  
  
 [in] `dwStyle`  
 The toolbar style. See [Toolbar Control and Button Styles](http://msdn.microsoft.com/library/windows/desktop/bb760439) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)] for the list of styles.  
  
 [in] `nID`  
 The ID of the child window of the toolbar.  
  
## Return Value  
 `TRUE` if this method succeeds; otherwise `FALSE`.  
  
## Remarks  
 This method creates a control bar and attaches it to the toolbar. It creates the control bar with the `TBSTYLE_FLAT` style. Call [CMFCToolBar::CreateEx](../vs140/CMFCToolBar--CreateEx.md) if you want a different control bar style.  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBar::CreateEx](../vs140/CMFCToolBar--CreateEx.md)