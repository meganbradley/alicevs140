---
title: "CScrollBar::Create"
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
ms.assetid: c4c51067-d48d-4f05-bb93-7ac8f5ad53f0
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CScrollBar::Create
Creates the Windows scroll bar and attaches it to the `CScrollBar` object.  
  
## Syntax  
  
```  
  
      virtual BOOL Create(  
   DWORD dwStyle,  
   const RECT& rect,  
   CWnd* pParentWnd,  
   UINT nID   
);  
```  
  
#### Parameters  
 `dwStyle`  
 Specifies the scroll bar's style. Apply any combination of [scroll-bar styles](../vs140/Scroll-Bar-Styles.md) to the scroll bar.  
  
 `rect`  
 Specifies the scroll bar's size and position. Can be either a `RECT` structure or a `CRect` object.  
  
 `pParentWnd`  
 Specifies the scroll bar's parent window, usually a `CDialog` object. It must not be **NULL**.  
  
 `nID`  
 The scroll bar's control ID.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 You construct a `CScrollBar` object in two steps. First, call the constructor, which constructs the `CScrollBar` object; then call **Create**, which creates and initializes the associated Windows scroll bar and attaches it to the `CScrollBar` object.  
  
 Apply the following [window styles](../vs140/Window-Styles.md) to a scroll bar:  
  
-   **WS_CHILD** Always  
  
-   **WS_VISIBLE** Usually  
  
-   **WS_DISABLED** Rarely  
  
-   **WS_GROUP** To group controls  
  
## Example  
 [!CODE [NVC_MFC_CScrollBar#1](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CScrollBar#1)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CScrollBar Class](../vs140/CScrollBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CScrollBar::CScrollBar](../vs140/CScrollBar--CScrollBar.md)