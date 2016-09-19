---
title: "CButton::Create"
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
ms.assetid: a6c736bf-0044-4bce-bd88-4ea8127b4d40
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CButton::Create
Creates the Windows button control and attaches it to the `CButton` object.  
  
## Syntax  
  
```  
  
      virtual BOOL Create(  
   LPCTSTR lpszCaption,  
   DWORD dwStyle,  
   const RECT& rect,  
   CWnd* pParentWnd,  
   UINT nID   
);  
```  
  
#### Parameters  
 `lpszCaption`  
 Specifies the button control's text.  
  
 `dwStyle`  
 Specifies the button control's style. Apply any combination of [button styles](../vs140/Button-Styles.md) to the button.  
  
 `rect`  
 Specifies the button control's size and position. It can be either a `CRect` object or a `RECT` structure.  
  
 `pParentWnd`  
 Specifies the button control's parent window, usually a `CDialog`. It must not be **NULL**.  
  
 `nID`  
 Specifies the button control's ID.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 You construct a `CButton` object in two steps. First, call the constructor and then call **Create**, which creates the Windows button control and attaches it to the `CButton` object.  
  
 If the **WS_VISIBLE** style is given, Windows sends the button control all the messages required to activate and show the button.  
  
 Apply the following [window styles](../vs140/Window-Styles.md) to a button control:  
  
-   **WS_CHILD** Always  
  
-   **WS_VISIBLE** Usually  
  
-   **WS_DISABLED** Rarely  
  
-   **WS_GROUP** To group controls  
  
-   **WS_TABSTOP** To include the button in the tabbing order  
  
## Example  
 [!CODE [NVC_MFC_CButton#2](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CButton#2)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CButton Class](../vs140/CButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CButton::CButton](../vs140/CButton--CButton.md)