---
title: "CDialog::OnOK"
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
ms.assetid: 78ca29b6-d9cf-44e6-ac6f-37a046e876e3
caps.latest.revision: 23
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDialog::OnOK
Called when the user clicks the **OK** button (the button with an ID of IDOK).  
  
## Syntax  
  
```  
virtual void OnOK( );  
```  
  
## Remarks  
 Override this method to perform actions when the **OK** button is activated. If the dialog box includes automatic data validation and exchange, the default implementation of this method validates the dialog box data and updates the appropriate variables in your application.  
  
 If you implement the **OK** button in a modeless dialog box, you must override the `OnOK` method and call [DestroyWindow](../vs140/CWnd--DestroyWindow.md) inside it. Do not call the base-class method, because it calls [EndDialog](../vs140/CDialog--EndDialog.md) which makes the dialog box invisible but does not destroy it.  
  
> [!NOTE]
>  You cannot override this method when you use a `CFileDialog` object in a program that is compiled under Windows XP. For more information about `CFileDialog`, see [CFileDialog Class](../vs140/CFileDialog-Class.md).  
  
## Example  
 [!CODE [NVC_MFCControlLadenDialog#68](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCControlLadenDialog#68)]  
  
## Requirements  
 `Header:` afxwin.h  
  
## See Also  
 [CDialog Class](../vs140/CDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDialog::OnCancel](../vs140/CDialog--OnCancel.md)   
 [CDialog::EndDialog](../vs140/CDialog--EndDialog.md)