---
title: "COleLinksDialog::DoModal"
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
ms.assetid: 00a76c98-39df-45ad-ba04-2a8ba15205a8
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleLinksDialog::DoModal
Displays the OLE Edit Links dialog box.  
  
## Syntax  
  
```  
  
virtual INT_PTR DoModal();  
```  
  
## Return Value  
 Completion status for the dialog box. One of the following values:  
  
-   **IDOK** if the dialog box was successfully displayed.  
  
-   **IDCANCEL** if the user canceled the dialog box.  
  
-   **IDABORT** if an error occurred. If **IDABORT** is returned, call the `COleDialog::GetLastError` member function to get more information about the type of error that occurred. For a listing of possible errors, see the [OleUIEditLinks](http://msdn.microsoft.com/library/windows/desktop/ms679703) function in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Remarks  
 If you want to initialize the various dialog box controls by setting members of the [m_el](../vs140/COleLinksDialog--m_el.md) structure, you should do it before calling `DoModal`, but after the dialog object is constructed.  
  
## Requirements  
 **Header:** afxodlgs.h  
  
## See Also  
 [COleLinksDialog Class](../vs140/COleLinksDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDialog::GetLastError](../vs140/COleDialog--GetLastError.md)   
 [CDialog::DoModal](../vs140/CDialog--DoModal.md)   
 [COleLinksDialog::m_el](../vs140/COleLinksDialog--m_el.md)