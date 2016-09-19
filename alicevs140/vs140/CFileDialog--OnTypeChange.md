---
title: "CFileDialog::OnTypeChange"
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
ms.assetid: b6bab10e-e07d-4358-9116-58a67226866a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFileDialog::OnTypeChange
Override this function to handle the **WM_NOTIFY CDN_TYPECHANGE** message.  
  
## Syntax  
  
```  
  
virtual void OnTypeChange( );  
```  
  
## Remarks  
 The notification message is sent when the user selects a new file type from the list of file types in the Open or Save As dialog box.  
  
 Notification is sent only if the dialog box was created with the OFN_EXPLORER style. For more information about the notification, see [CDN_TYPECHANGE](http://msdn.microsoft.com/library/windows/desktop/ms646868). For information about the OFN_EXPLORER style, see the [OPENFILENAME](http://msdn.microsoft.com/library/windows/desktop/ms646839) structure and [Open and Save As Dialog Boxes](http://msdn.microsoft.com/library/windows/desktop/ms646960).  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CFileDialog Class](../vs140/CFileDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFileDialog::OnFolderChange](../vs140/CFileDialog--OnFolderChange.md)