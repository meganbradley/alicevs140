---
title: "CDialog::OnInitDialog"
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
ms.assetid: 76d86e5f-435d-44d0-89ec-c2296367d058
caps.latest.revision: 22
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDialog::OnInitDialog
This method is called in response to the `WM_INITDIALOG` message.  
  
## Syntax  
  
```  
virtual BOOL OnInitDialog( );  
```  
  
## Return Value  
 Specifies whether the application has set the input focus to one of the controls in the dialog box. If `OnInitDialog` returns nonzero, Windows sets the input focus to the default location, the first control in the dialog box. The application can return 0 only if it has explicitly set the input focus to one of the controls in the dialog box.  
  
## Remarks  
 Windows sends the `WM_INITDIALOG` message to the dialog box during the [Create](../vs140/CDialog--Create.md), [CreateIndirect](../vs140/CDialog--CreateIndirect.md), or [DoModal](../vs140/CDialog--DoModal.md) calls, which occur immediately before the dialog box is displayed.  
  
 Override this method if you want to perform special processing when the dialog box is initialized. In the overridden version, first call the base class `OnInitDialog` but ignore its return value. You will typically return `TRUE` from your overridden method.  
  
 Windows calls the `OnInitDialog` function by using the standard global dialog-box procedure common to all Microsoft Foundation Class Library dialog boxes. It does not call this function through your message map, and therefore you do not need a message map entry for this method.  
  
> [!NOTE]
>  You cannot override this method when you use a `CFileDialog` object in a program that is compiled under [!INCLUDE[wiprlhext](../vs140/includes/wiprlhext_md.md)]. For more information about changes to `CFileDialog` under [!INCLUDE[wiprlhext](../vs140/includes/wiprlhext_md.md)] see [CFileDialog Class](../vs140/CFileDialog-Class.md).  
  
## Example  
 [!CODE [NVC_MFCControlLadenDialog#67](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCControlLadenDialog#67)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDialog Class](../vs140/CDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDialog::Create](../vs140/CDialog--Create.md)   
 [CDialog::CreateIndirect](../vs140/CDialog--CreateIndirect.md)   
 [WM_INITDIALOG](http://msdn.microsoft.com/library/windows/desktop/ms645428)