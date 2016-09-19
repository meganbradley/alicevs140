---
title: "CMFCToolBar::CreateEx"
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
ms.assetid: b348ea2e-68ae-47d2-8919-767c2b3f4749
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::CreateEx
Creates a `CMFCToolBar` object that uses additional style options, such as large icons.  
  
## Syntax  
  
```  
virtual BOOL CreateEx(  
   CWnd* pParentWnd,  
   DWORD dwCtrlStyle=TBSTYLE_FLAT,  
   DWORD dwStyle=AFX_DEFAULT_TOOLBAR_STYLE,  
   CRect rcBorders=CRect(1, 1, 1, 1),  
   UINT nID=AFX_IDW_TOOLBAR   
);  
```  
  
#### Parameters  
 [in] `pParentWnd`  
 A pointer to the parent window of the toolbar.  
  
 [in] `dwCtrlStyle`  
 Additional styles for creating the embedded control bar object.  
  
 [in] `dwStyle`  
 The toolbar style. See [Toolbar Control and Button Styles](http://msdn.microsoft.com/library/windows/desktop/bb760439) for a list of appropriate styles.  
  
 [in] `rcBorders`  
 A `CRect` object that specifies the widths of the toolbar window borders.  
  
 [in] `nID`  
 The ID of the child window of the toolbar.  
  
## Return Value  
 Nonzero if this method succeeds; otherwise 0.  
  
## Remarks  
 This method creates a control bar and attaches it to the toolbar.  
  
 Call this method instead of [CMFCToolBar::Create](../vs140/CMFCToolBar--Create.md) when you want to provide specific styles. For example, set `dwCtrlStyle` to `TBSTYLE_FLAT | TBSTYLE_TRANSPARENT` to create a toolbar that resembles the toolbars that are used by Internet Explorer 4.  
  
## Example  
 The following example demonstrates how to use the `CreateEx` method of the `CMFCToolBar` class. This code snippet is part of the [IE Demo sample](../vs140/Visual-C---Samples.md).  
  
 [!CODE [NVC_MFC_IEDemo#6](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_IEDemo#6)]  
[!CODE [NVC_MFC_IEDemo#7](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_IEDemo#7)]  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBar::Create](../vs140/CMFCToolBar--Create.md)