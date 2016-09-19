---
title: "COlePasteSpecialDialog::DoModal"
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
ms.assetid: 3d71b4f3-5764-4479-b6d2-627f6c448ea0
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COlePasteSpecialDialog::DoModal
Displays the OLE Paste Special dialog box.  
  
## Syntax  
  
```  
  
virtual INT_PTR DoModal( );  
```  
  
## Return Value  
 Completion status for the dialog box. One of the following values:  
  
-   **IDOK** if the dialog box was successfully displayed.  
  
-   **IDCANCEL** if the user canceled the dialog box.  
  
-   **IDABORT** if an error occurred. If **IDABORT** is returned, call the `COleDialog::GetLastError` member function to get more information about the type of error that occurred. For a listing of possible errors, see the [OleUIPasteSpecial](http://msdn.microsoft.com/library/windows/desktop/ms694512) function in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Remarks  
 If you want to initialize the various dialog box controls by setting members of the [m_ps](../vs140/COlePasteSpecialDialog--m_ps.md) structure, you should do this before calling `DoModal`, but after the dialog object is constructed.  
  
 If `DoModal` returns **IDOK**, you can call other member functions to retrieve the settings or information input by the user into the dialog box.  
  
## Requirements  
 **Header:** afxodlgs.h  
  
## See Also  
 [COlePasteSpecialDialog Class](../vs140/COlePasteSpecialDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDataObject Class](../vs140/COleDataObject-Class.md)   
 [COleDialog::GetLastError](../vs140/COleDialog--GetLastError.md)   
 [CDialog::DoModal](../vs140/CDialog--DoModal.md)   
 [COlePasteSpecialDialog::COlePasteSpecialDialog](../vs140/COlePasteSpecialDialog--COlePasteSpecialDialog.md)   
 [COlePasteSpecialDialog::GetDrawAspect](../vs140/COlePasteSpecialDialog--GetDrawAspect.md)   
 [COlePasteSpecialDialog::GetIconicMetafile](../vs140/COlePasteSpecialDialog--GetIconicMetafile.md)   
 [COlePasteSpecialDialog::GetPasteIndex](../vs140/COlePasteSpecialDialog--GetPasteIndex.md)   
 [COlePasteSpecialDialog::GetSelectionType](../vs140/COlePasteSpecialDialog--GetSelectionType.md)