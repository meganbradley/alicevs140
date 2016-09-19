---
title: "CMFCMenuBar::Create"
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
ms.assetid: b94c09d0-6836-4870-8710-bd63467f4fbb
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCMenuBar::Create
Creates a menu control and attaches it to a [CMFCMenuBar](../vs140/CMFCMenuBar-Class.md) object.  
  
## Syntax  
  
```  
virtual BOOL Create(  
   CWnd* pParentWnd,  
   DWORD dwStyle = AFX_DEFAULT_TOOLBAR_STYLE,  
   UINT nID = AFX_IDW_MENUBAR  
);  
```  
  
#### Parameters  
 [in] `pParentWnd`  
 Pointer to the parent window for the new `CMFCMenuBar` object.  
  
 [in] `dwStyle`  
 The style of the new menu bar.  
  
 [in] `nID`  
 The ID for the child window of the menu bar.  
  
## Return Value  
 `TRUE` if successful; otherwise `FALSE`.  
  
## Remarks  
 After you construct a `CMFCMenuBar` object, you must call `Create`. This method creates the `CMFCMenuBar` control and attaches it to the `CMFCMenuBar` object.  
  
 For more information about toolbar styles, see [CBasePane::SetPaneStyle](../vs140/CBasePane--SetPaneStyle.md).  
  
## Requirements  
 **Header:** afxmenubar.h  
  
## See Also  
 [CMFCMenuBar Class](../vs140/CMFCMenuBar-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)