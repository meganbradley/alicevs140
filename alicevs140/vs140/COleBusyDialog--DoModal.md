---
title: "COleBusyDialog::DoModal"
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
ms.assetid: 8142f3d7-0dad-4af2-b06a-1592ebd6ebe0
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleBusyDialog::DoModal
Call this function to display the OLE Server Busy or Server Not Responding dialog box.  
  
## Syntax  
  
```  
  
virtual INT_PTR DoModal( );  
```  
  
## Return Value  
 Completion status for the dialog box. One of the following values:  
  
-   **IDOK** if the dialog box was successfully displayed.  
  
-   **IDCANCEL** if the user canceled the dialog box.  
  
-   **IDABORT** if an error occurred. If **IDABORT** is returned, call the `COleDialog::GetLastError` member function to get more information about the type of error that occurred. For a listing of possible errors, see the [OleUIBusy](http://msdn.microsoft.com/library/windows/desktop/ms680125) function in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Remarks  
 If you want to initialize the various dialog box controls by setting members of the [m_bz](../vs140/COleBusyDialog--m_bz.md) structure, you should do this before calling `DoModal`, but after the dialog object is constructed.  
  
 If `DoModal` returns **IDOK**, you can call other member functions to retrieve the settings or information that was input by the user into the dialog box.  
  
## Requirements  
 **Header:** afxodlgs.h  
  
## See Also  
 [COleBusyDialog Class](../vs140/COleBusyDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDialog::GetLastError](../vs140/COleDialog--GetLastError.md)   
 [CDialog::DoModal](../vs140/CDialog--DoModal.md)   
 [COleBusyDialog::GetSelectionType](../vs140/COleBusyDialog--GetSelectionType.md)   
 [COleBusyDialog::m_bz](../vs140/COleBusyDialog--m_bz.md)