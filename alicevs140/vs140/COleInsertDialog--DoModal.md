---
title: "COleInsertDialog::DoModal"
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
ms.assetid: f7c225e7-bf00-4530-9997-e484fffe1f0c
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleInsertDialog::DoModal
Call this function to display the OLE Insert Object dialog box.  
  
## Syntax  
  
```  
virtual INT_PTR   
   DoModal();  
INT_PTR   
   DoModal(  
   DWORD dwFlags   
);  
```  
  
#### Parameters  
 `dwFlags`  
 One of the following values:  
  
 `COleInsertDialog::DocObjectsOnly` inserts only DocObjects.  
  
 `COleInsertDialog::ControlsOnly` inserts only ActiveX controls.  
  
 Zero inserts neither a DocObject nor an ActiveX control. This value results in the same implementation as the first prototype listed above.  
  
## Return Value  
 Completion status for the dialog box. One of the following values:  
  
-   IDOK if the dialog box was successfully displayed.  
  
-   IDCANCEL if the user canceled the dialog box.  
  
-   IDABORT if an error occurred. If IDABORT is returned, call the [COleDialog::GetLastError](../vs140/COleDialog--GetLastError.md) member function to get more information about the type of error that occurred. For a listing of possible errors, see the [OleUIInsertObject](http://msdn.microsoft.com/library/windows/desktop/ms694325) function in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Remarks  
 If you want to initialize the various dialog box controls by setting members of the [m_io](../vs140/COleInsertDialog--m_io.md) structure, you should do this before calling `DoModal`, but after the dialog object is constructed.  
  
 If `DoModal` returns IDOK, you can call other member functions to retrieve the settings or information input into the dialog box by the user.  
  
## Requirements  
 **Header:** afxodlgs.h  
  
## See Also  
 [COleInsertDialog Class](../vs140/COleInsertDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDialog::GetLastError](../vs140/COleDialog--GetLastError.md)   
 [CDialog::DoModal](../vs140/CDialog--DoModal.md)   
 [COleInsertDialog::GetSelectionType](../vs140/COleInsertDialog--GetSelectionType.md)   
 [COleInsertDialog::GetClassID](../vs140/COleInsertDialog--GetClassID.md)   
 [COleInsertDialog::GetDrawAspect](../vs140/COleInsertDialog--GetDrawAspect.md)   
 [COleInsertDialog::GetIconicMetafile](../vs140/COleInsertDialog--GetIconicMetafile.md)   
 [COleInsertDialog::GetPathName](../vs140/COleInsertDialog--GetPathName.md)   
 [COleInsertDialog::m_io](../vs140/COleInsertDialog--m_io.md)