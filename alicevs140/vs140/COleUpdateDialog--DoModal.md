---
title: "COleUpdateDialog::DoModal"
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
ms.assetid: 3a26df9f-5ddf-4ff1-aac0-f26a4e7a6daa
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleUpdateDialog::DoModal
Displays the Edit Links dialog box in update mode.  
  
## Syntax  
  
```  
  
virtual INT_PTR DoModal( );  
```  
  
## Return Value  
 Completion status for the dialog box. One of the following values:  
  
-   **IDOK** if the dialog box returned successfully.  
  
-   **IDCANCEL** if none of the linked or embedded items in the current document need updating.  
  
-   **IDABORT** if an error occurred. If **IDABORT** is returned, call the [COleDialog::GetLastError](../vs140/COleDialog--GetLastError.md) member function to get more information about the type of error that occurred. For a listing of possible errors, see the [OleUIEditLinks](http://msdn.microsoft.com/library/windows/desktop/ms679703) function in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Remarks  
 All links and/or embeddings are updated unless the user selects the Cancel button.  
  
## Requirements  
 **Header:** afxodlgs.h  
  
## See Also  
 [COleUpdateDialog Class](../vs140/COleUpdateDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDialog::GetLastError](../vs140/COleDialog--GetLastError.md)   
 [COleLinksDialog::DoModal](../vs140/COleLinksDialog--DoModal.md)