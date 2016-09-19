---
title: "CFileDialog::OnFileNameChange"
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
ms.assetid: fc7f7410-5955-49f1-8691-cf5d92a43f4e
caps.latest.revision: 24
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFileDialog::OnFileNameChange
Override this method if you want to handle the `WM_NOTIFY` `CDN_SELCHANGE` message.  
  
## Syntax  
  
```  
virtual void OnFileNameChange( );  
```  
  
## Remarks  
 The system sends the `CDN_SELCHANGE` message when the user selects a new file or folder in the file list of the **Open** or **Save As** dialog box. Override this method if you want to perform any actions in response to this message.  
  
 The system sends this message only if the dialog box was created with the OFN_EXPLORER flag turned on. For more information about the notification, see [CDN_SELCHANGE](http://msdn.microsoft.com/library/windows/desktop/ms646865). For information about the OFN_EXPLORER flag, see the [OPENFILENAME](http://msdn.microsoft.com/library/windows/desktop/ms646839) structure and [Open and Save As Dialog Boxes](http://msdn.microsoft.com/library/windows/desktop/ms646960).  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CFileDialog Class](../vs140/CFileDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFileDialog::OnFolderChange](../vs140/CFileDialog--OnFolderChange.md)