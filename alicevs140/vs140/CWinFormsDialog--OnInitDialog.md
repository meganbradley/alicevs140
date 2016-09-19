---
title: "CWinFormsDialog::OnInitDialog"
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
ms.assetid: 70ccd31c-cef5-4312-b975-3fc3ea15e042
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinFormsDialog::OnInitDialog
Initializes the MFC dialog box by creating and hosting a Windows Forms user control on it.  
  
## Syntax  
  
```  
virtual BOOL OnInitDialog();  
```  
  
## Return Value  
 A boolean value that specifies whether the application has set the input focus to one of the controls in the dialog box. If `OnInitDialog` returns nonzero, Windows sets the input focus to the first control in the dialog box. This method can return 0 only if the application has explicitly set the input focus to one of the controls in the dialog box.  
  
## Remarks  
 When the MFC dialog box is created (using the [Create](../vs140/CDialog--Create.md), [CreateIndirect](../vs140/CDialog--CreateIndirect.md), or [DoModal](../vs140/CDialog--DoModal.md) method inherited from [CDialog](../vs140/CDialog-Class.md)), a `WM_INITDIALOG` message is sent and this method is called. It creates an instance of a <xref:System.Windows.Forms.UserControl?qualifyHint=False> control on the dialog box and adjusts the size of the dialog box to accommodate for the size of the user control. Then it hosts the new control in the MFC dialog box.  
  
 Override this member function if you need to perform special processing when the dialog box is initialized. For more information on using this method, see [CDialog::OnInitDialog](../vs140/CDialog--OnInitDialog.md).  
  
## Requirements  
 **Header:** afxwinforms.h  
  
## See Also  
 <xref:System.Windows.Forms.UserControl?qualifyHint=True>   
 [CWinFormsDialog Overview](../Topic/CWinFormsDialog%20Class.md)   
 [CDialog::OnInitDialog](../vs140/CDialog--OnInitDialog.md)