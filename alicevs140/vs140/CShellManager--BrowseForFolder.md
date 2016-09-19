---
title: "CShellManager::BrowseForFolder"
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
ms.assetid: 89a9a3e8-c4b9-42a0-990e-a384d51abb4a
caps.latest.revision: 18
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CShellManager::BrowseForFolder
Displays a dialog box that enables the user to select a shell folder.  
  
## Syntax  
  
```  
BOOL BrowseForFolder(  
   CString& strOutFolder,  
   CWnd* pWndParent = NULL,  
   LPCTSTR lplszInitialFolder = NULL,  
   LPCTSTR lpszTitle = NULL,  
   UINT ulFlags = BIF_RETURNONLYFSDIRS,  
   LPINT piFolderImage = NULL  
);  
```  
  
#### Parameters  
 [out] `strOutFolder`  
 The string used by the method to store the path of the selected folder.  
  
 [in] `pWndParent`  
 A pointer to the parent window.  
  
 [in] `lplszInitialFolder`  
 A string that contains the folder that is selected by default when the dialog box is displayed.  
  
 [in] `lpszTitle`  
 The title for the dialog box.  
  
 [in] `ulFlags`  
 Flags specifying options for the dialog box. See [BROWSEINFO](http://msdn.microsoft.com/library/windows/desktop/bb773205) for the detailed description.  
  
 [out] `piFolderImage`  
 A pointer to the integer value where the method writes the image index of the selected folder.  
  
## Return Value  
 Nonzero if the user selects a folder from the dialog box; otherwise 0.  
  
## Remarks  
 When you call this method, the application creates and shows a dialog box that enables the user to select a folder. The method will write the path of the folder into the `strOutFolder` parameter.  
  
## Example  
 The following example demonstrates how to retrieve a reference to a `CShellManager` object by using the `CWinAppEx::GetShellManager` method and how to use the `BrowseForFolder` method. This code snippet is part of the [Explorer sample](../vs140/Visual-C---Samples.md).  
  
 [!CODE [NVC_MFC_Explorer#6](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_Explorer#6)]  
  
## Requirements  
 **Header:** afxshellmanager.h  
  
## See Also  
 [CShellManager Class](../vs140/CShellManager-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)