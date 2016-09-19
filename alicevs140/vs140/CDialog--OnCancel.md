---
title: "CDialog::OnCancel"
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
ms.assetid: 01b6fadd-183c-481d-9a9b-4da64213b1c2
caps.latest.revision: 23
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDialog::OnCancel
The framework calls this method when the user clicks **Cancel** or presses the ESC key in a modal or modeless dialog box.  
  
## Syntax  
  
```  
virtual void OnCancel( );  
```  
  
## Remarks  
 Override this method to perform actions (such as restoring old data) when a user closes the dialog box by clicking **Cancel** or hitting the ESC key. The default closes a modal dialog box by calling [EndDialog](../vs140/CDialog--EndDialog.md) and causing [DoModal](../vs140/CDialog--DoModal.md) to return IDCANCEL.  
  
 If you implement the **Cancel** button in a modeless dialog box, you must override the `OnCancel` method and call [DestroyWindow](../vs140/CWnd--DestroyWindow.md) inside it. Do not call the base-class method, because it calls `EndDialog`, which will make the dialog box invisible but not destroy it.  
  
> [!NOTE]
>  You cannot override this method when you use a `CFileDialog` object in a program that is compiled under Windows XP. For more information about `CFileDialog`, see [CFileDialog Class](../vs140/CFileDialog-Class.md).  
  
## Example  
 [!CODE [NVC_MFCControlLadenDialog#66](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCControlLadenDialog#66)]  
  
## Requirements  
 `Header:` afxwin.h  
  
## See Also  
 [CDialog Class](../vs140/CDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDialog::OnOK](../vs140/CDialog--OnOK.md)   
 [CDialog::EndDialog](../vs140/CDialog--EndDialog.md)