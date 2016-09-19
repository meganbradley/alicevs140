---
title: "CMFCOutlookBar::Create"
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
ms.assetid: 7dbce5a5-bc78-456f-aebb-2fafa4ffc890
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCOutlookBar::Create
Creates the Outlook bar control.  
  
## Syntax  
  
```  
virtual BOOL Create(  
   LPCTSTR lpszCaption,  
   CWnd* pParentWnd,  
   const RECT& rect,  
   UINT nID,  
   DWORD dwStyle,  
   DWORD dwControlBarStyle=AFX_CBRS_RESIZE,  
   CCreateContext* pContext=NULL   
);  
```  
  
#### Parameters  
 [in] `lpszCaption`  
 Specifies the window caption.  
  
 [in] `pParentWnd`  
 Specifies a pointer to a parent window. It must not be NULL.  
  
 [in] `rect`  
 Specifies the outlook bar size and position in pixels.  
  
 [in] `nID`  
 Specifies the control ID. Must be distinct from other control IDs used in the application.  
  
 [in] `dwStyle`  
 Specifies the desired control bar style. For possible values, see [Window Styles](../vs140/Window-Styles.md).  
  
 [in] `dwControlBarStyle`  
 Specifies the special library-defined styles.  
  
 [in] `pContext`  
 Create context.  
  
## Return Value  
 Nonzero if the method is successful; otherwise 0.  
  
## Remarks  
 You construct a `CMFCOutlookBar` object in two steps. First call the constructor, and then call `Create`, which creates the outlook bar control and attaches it to the `CMFCOutlookBar` object.  
  
 See [CBasePane::CreateEx](../vs140/CBasePane--CreateEx.md) for the list of the available library-defined styles to be specified by `dwControlBarStyle`.  
  
## Example  
 The following example demonstrates how to use the `Create` method of the `CMFCOutlookBar` class. This code snippet is part of the [Outlook Multi Views sample](../vs140/Visual-C---Samples.md).  
  
 [!CODE [NVC_MFC_OutlookMultiViews#1](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_OutlookMultiViews#1)]  
[!CODE [NVC_MFC_OutlookMultiViews#2](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_OutlookMultiViews#2)]  
  
## Requirements  
 **Header:** afxoutlookbar.h  
  
## See Also  
 [CMFCOutlookBar Class](../vs140/CMFCOutlookBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)