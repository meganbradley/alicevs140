---
title: "CFileDialog::GetFolderPath"
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
ms.assetid: cf883b6d-4f7d-4418-b76f-b3f50046d6bb
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFileDialog::GetFolderPath
Call this member function to retrieve the path of the currently open folder or directory for an Explorer-style Open or Save As common dialog box.  
  
## Syntax  
  
```  
  
CString GetFolderPath( ) const;  
  
```  
  
## Return Value  
 A [CString](../vs140/CStringT-Class.md) object containing the currently open folder or directory.  
  
## Remarks  
 The dialog box must have been created with the **OFN_EXPLORER** style; otherwise, the method will fail with an assertion.  
  
 You can call this method only while the dialog box is being displayed. After the dialog box has been closed, this function will no longer work, and the method will fail with an assertion.  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CFileDialog Class](../vs140/CFileDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDM_GETFOLDERPATH](http://msdn.microsoft.com/library/windows/desktop/ms646850)