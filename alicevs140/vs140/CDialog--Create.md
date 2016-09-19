---
title: "CDialog::Create"
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
ms.assetid: df6bd976-0166-497c-bd33-3f33c1738877
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDialog::Create
Call **Create** to create a modeless dialog box using a dialog-box template from a resource.  
  
## Syntax  
  
```  
  
      virtual BOOL Create(  
   LPCTSTR lpszTemplateName,  
   CWnd* pParentWnd = NULL   
);  
virtual BOOL Create(  
   UINT nIDTemplate,  
   CWnd* pParentWnd = NULL   
);  
```  
  
#### Parameters  
 `lpszTemplateName`  
 Contains a null-terminated string that is the name of a dialog-box template resource.  
  
 `pParentWnd`  
 Points to the parent window object (of type [CWnd](../vs140/CWnd-Class.md)) to which the dialog object belongs. If it is **NULL**, the dialog object's parent window is set to the main application window.  
  
 `nIDTemplate`  
 Contains the ID number of a dialog-box template resource.  
  
## Return Value  
 Both forms return nonzero if dialog-box creation and initialization were successful; otherwise 0.  
  
## Remarks  
 You can put the call to **Create** inside the constructor or call it after the constructor is invoked.  
  
 Two forms of the **Create** member function are provided for access to the dialog-box template resource by either template name or template ID number (for example, IDD_DIALOG1).  
  
 For either form, pass a pointer to the parent window object. If `pParentWnd` is **NULL**, the dialog box will be created with its parent or owner window set to the main application window.  
  
 The **Create** member function returns immediately after it creates the dialog box.  
  
 Use the **WS_VISIBLE** style in the dialog-box template if the dialog box should appear when the parent window is created. Otherwise, you must call `ShowWindow`. For further dialog-box styles and their application, see the [DLGTEMPLATE](http://msdn.microsoft.com/library/windows/desktop/ms645394) structure in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)] and [Window Styles](../vs140/Window-Styles.md) in the *MFC Reference*.  
  
 Use the `CWnd::DestroyWindow` function to destroy a dialog box created by the **Create** function.  
  
## Example  
 [!CODE [NVC_MFCControlLadenDialog#62](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCControlLadenDialog#62)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDialog Class](../vs140/CDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDialog::CDialog](../vs140/CDialog--CDialog.md)   
 [CWnd::DestroyWindow](../vs140/CWnd--DestroyWindow.md)   
 [CDialog::InitModalIndirect](../vs140/CDialog--InitModalIndirect.md)   
 [CDialog::DoModal](../vs140/CDialog--DoModal.md)   
 [CreateDialog](http://msdn.microsoft.com/library/windows/desktop/ms645434)