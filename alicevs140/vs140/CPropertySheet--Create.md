---
title: "CPropertySheet::Create"
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
ms.assetid: e2fb8a7d-40ca-4736-acce-734b6f92316e
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPropertySheet::Create
Displays a modeless property sheet.  
  
## Syntax  
  
```  
  
      virtual BOOL Create(  
   CWnd* pParentWnd = NULL,  
   DWORD dwStyle = (DWORD)–1,  
   DWORD dwExStyle = 0   
);  
```  
  
#### Parameters  
 `pParentWnd`  
 Points to parent window. If **NULL**, parent is the desktop.  
  
 `dwStyle`  
 Window styles for property sheet. For a complete list of available styles, see [Window Styles](../vs140/Window-Styles.md).  
  
 `dwExStyle`  
 Extended window styles for property sheet. For a complete list of available styles, see [Extended Window Styles](../vs140/Extended-Window-Styles.md)  
  
## Return Value  
 Nonzero if the property sheet is created successfully; otherwise 0.  
  
## Remarks  
 The call to **Create** can be inside the constructor, or you can call it after the constructor is invoked.  
  
 The default style, expressed by passing –1 as `dwStyle`, is actually **WS_SYSMENU &#124;** `WS_POPUP` **&#124; WS_CAPTION &#124; DS_MODALFRAME &#124; DS_CONTEXTHELP &#124; WS_VISIBLE**. The default extended window style, expressed by passing 0 as `dwExStyle`, is actually **WS_EX_DLGMODALFRAME**.  
  
 The **Create** member function returns immediately after creating the property sheet. To destroy the property sheet, call [CWnd::DestroyWindow](../vs140/CWnd--DestroyWindow.md).  
  
 Modeless property sheets displayed with a call to **Create** do not have OK, Cancel, Apply Now, and Help buttons as modal property sheets do. Desired buttons must be created by the user.  
  
 To display a modal property sheet, call [DoModal](../vs140/CPropertySheet--DoModal.md) instead.  
  
## Example  
 [!CODE [NVC_MFCDocView#132](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#132)]  
  
 [!CODE [NVC_MFCDocView#133](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#133)]  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CPropertySheet Class](../vs140/CPropertySheet-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDialog::Create](../vs140/CDialog--Create.md)   
 [CPropertySheet::DoModal](../vs140/CPropertySheet--DoModal.md)