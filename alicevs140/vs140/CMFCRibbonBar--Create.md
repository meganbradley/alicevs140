---
title: "CMFCRibbonBar::Create"
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
ms.assetid: fbb4c188-4077-42b8-9559-86b32ca5d03c
caps.latest.revision: 28
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonBar::Create
Creates a window for the ribbon bar.  
  
## Syntax  
  
```  
BOOL Create(  
   CWnd* pParentWnd,  
   DWORD dwStyle = WS_CHILD | WS_VISIBLE | CBRS_TOP,  
   UINT nID = AFX_IDW_RIBBON_BAR   
);  
```  
  
#### Parameters  
 [in] `pParentWnd`  
 Pointer to the parent window for the ribbon bar.  
  
 [in] `dwStyle`  
 A logical combination of styles for the new window.  
  
 [in] `nID`  
 ID of the new window.  
  
## Return Value  
 `TRUE` if the window was created; otherwise `FALSE`.  
  
## Remarks  
  
## Example  
 The following example demonstrates how to use the `Create` method of the `CMFCRibbonBar` class.  
  
 [!CODE [NVC_MFC_RibbonApp#1](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_RibbonApp#1)]  
  
## Requirements  
 **Header:** afxribbonbar.h  
  
## See Also  
 [CMFCRibbonBar Class](../vs140/CMFCRibbonBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)