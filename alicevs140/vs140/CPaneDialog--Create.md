---
title: "CPaneDialog::Create"
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
ms.assetid: bd7499e3-4273-4705-8bca-719b512c668a
caps.latest.revision: 18
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPaneDialog::Create
Creates a docking dialog box and attaches it to a `CPaneDialog` object.  
  
## Syntax  
  
```  
BOOL Create(  
   LPCTSTR lpszWindowName,  
   CWnd* pParentWnd,  
   BOOL bHasGripper,  
   LPCTSTR lpszTemplateName,  
   UINT nStyle,  
   UINT nID,  
   DWORD dwTabbedStyle= AFX_CBRS_REGULAR_TABS,  
   DWORD dwControlBarStyle=AFX_DEFAULT_DOCKING_PANE_STYLE  
);  
BOOL Create(  
   LPCTSTR lpszWindowName,  
   CWnd* pParentWnd,  
   BOOL bHasGripper,  
   UINT nIDTemplate,  
   UINT nStyle,  
   UINT nID   
);  
BOOL Create(  
   CWnd* pParentWnd,  
   LPCTSTR lpszTemplateName,  
   UINT nStyle,  
   UINT nID   
);  
BOOL Create(  
   CWnd* pParentWnd,  
   UINT nIDTemplate,  
   UINT nStyle,  
   UINT nID   
);  
```  
  
#### Parameters  
 [in] `lpszWindowName`  
 The name of the docking dialog box.  
  
 [in] `pParentWnd`  
 Points to the parent window.  
  
 [in] `bHasGripper`  
 `TRUE` to create the docking dialog box with a caption (gripper); otherwise, `FALSE`.  
  
 [in] `lpszTemplateName`  
 The name of the resource dialog template.  
  
 [in] `nStyle`  
 The Windows style.  
  
 [in] `nID`  
 The control ID.  
  
 [in] `nIDTemplate`  
 The resource ID of the dialog template.  
  
 [in] `dwTabbedStyle`  
 The style of the tabbed window that results when the user drags another control pane onto the caption of this control pane. The default value is `AFX_CBRS_REGULAR_TABS`. For more information, see the Remarks section of the [CBasePane::CreateEx](../vs140/CBasePane--CreateEx.md) method.  
  
 [in] `dwControlBarStyle`  
 Additional style attributes. The default value is `AFX_DEFAULT_DOCKING_PANE_STYLE`. For more information, see the Remarks section of the [CBasePane::CreateEx](../vs140/CBasePane--CreateEx.md) method.  
  
## Return Value  
 `TRUE` if this method succeeds; otherwise, `FALSE`.  
  
## Remarks  
  
## Example  
 The following example demonstrates how to use the `Create` method in the `CPaneDialog` class. This example is part of the [Set Pane Size sample](../vs140/Visual-C---Samples.md).  
  
 [!CODE [NVC_MFC_SetPaneSize#2](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_SetPaneSize#2)]  
[!CODE [NVC_MFC_SetPaneSize#3](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_SetPaneSize#3)]  
  
## Requirements  
 **Header:** afxpanedialog.h  
  
## See Also  
 [CPaneDialog Class](../vs140/CPaneDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)