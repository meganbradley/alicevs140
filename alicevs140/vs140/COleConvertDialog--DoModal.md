---
title: "COleConvertDialog::DoModal"
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
ms.assetid: e383e972-945a-460c-b881-e7a7b2942bc8
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleConvertDialog::DoModal
Call this function to display the OLE Convert dialog box.  
  
## Syntax  
  
```  
  
virtual INT_PTR DoModal( );  
```  
  
## Return Value  
 Completion status for the dialog box. One of the following values:  
  
-   **IDOK** if the dialog box was successfully displayed.  
  
-   **IDCANCEL** if the user canceled the dialog box.  
  
-   **IDABORT** if an error occurred. If **IDABORT** is returned, call the [COleDialog::GetLastError](../vs140/COleDialog--GetLastError.md) member function to get more information about the type of error that occurred. For a listing of possible errors, see the [OleUIConvert](http://msdn.microsoft.com/library/windows/desktop/ms680694) function in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Remarks  
 If you want to initialize the various dialog box controls by setting members of the [m_cv](../vs140/COleConvertDialog--m_cv.md) structure, you should do this before calling `DoModal`, but after the dialog object is constructed.  
  
 If `DoModal` returns **IDOK**, you can call other member functions to retrieve the settings or information that was input by the user into the dialog box.  
  
## Requirements  
 **Header:** afxodlgs.h  
  
## See Also  
 [COleConvertDialog Class](../vs140/COleConvertDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDialog::GetLastError](../vs140/COleDialog--GetLastError.md)   
 [CDialog::DoModal](../vs140/CDialog--DoModal.md)   
 [COleConvertDialog::m_cv](../vs140/COleConvertDialog--m_cv.md)   
 [COleConvertDialog::DoConvert](../vs140/COleConvertDialog--DoConvert.md)   
 [COleConvertDialog::GetSelectionType](../vs140/COleConvertDialog--GetSelectionType.md)   
 [COleConvertDialog::GetClassID](../vs140/COleConvertDialog--GetClassID.md)   
 [COleConvertDialog::GetDrawAspect](../vs140/COleConvertDialog--GetDrawAspect.md)   
 [COleConvertDialog::GetIconicMetafile](../vs140/COleConvertDialog--GetIconicMetafile.md)