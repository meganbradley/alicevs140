---
title: "COleChangeSourceDialog::DoModal"
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
ms.assetid: d44aebc9-69da-41d4-a188-e7f1d007a0a9
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleChangeSourceDialog::DoModal
Call this function to display the OLE Change Source dialog box.  
  
## Syntax  
  
```  
  
virtual INT_PTR DoModal( );  
  
```  
  
## Return Value  
 Completion status for the dialog box. One of the following values:  
  
-   **IDOK** if the dialog box was successfully displayed.  
  
-   **IDCANCEL** if the user canceled the dialog box.  
  
-   **IDABORT** if an error occurred. If **IDABORT** is returned, call the [COleDialog::GetLastError](../vs140/COleDialog--GetLastError.md) member function to get more information about the type of error that occurred. For a listing of possible errors, see the [OleUIChangeSource](http://msdn.microsoft.com/library/windows/desktop/ms682497) function in [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Remarks  
 If you want to initialize the various dialog box controls by setting members of the [m_cs](../vs140/COleChangeSourceDialog--m_cs.md) structure, you should do this before calling `DoModal`, but after the dialog object is constructed.  
  
 If `DoModal` returns **IDOK**, you can call member functions to retrieve user-entered settings or information from the dialog box. The following list names typical query functions:  
  
-   [GetFileName](../vs140/COleChangeSourceDialog--GetFileName.md)  
  
-   [GetDisplayName](../vs140/COleChangeSourceDialog--GetDisplayName.md)  
  
-   [GetItemName](../vs140/COleChangeSourceDialog--GetItemName.md)  
  
## Requirements  
 **Header:** afxodlgs.h  
  
## See Also  
 [COleChangeSourceDialog Class](../vs140/COleChangeSourceDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleChangeSourceDialog::COleChangeSourceDialog](../vs140/COleChangeSourceDialog--COleChangeSourceDialog.md)