---
title: "CFileDialog::GetFileTitle"
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
ms.assetid: 94c5b0b7-a260-4521-a706-55172a476f9b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFileDialog::GetFileTitle
Call this function to retrieve the title of the file entered in the dialog box.  
  
## Syntax  
  
```  
  
CString GetFileTitle( ) const;  
```  
  
## Return Value  
 The title of the file.  
  
## Remarks  
 The title of the file includes only its prefix, without the path or the extension. For example, `GetFileTitle` will return "TEXT" for the file C:\FILES\TEXT.DAT.  
  
 If `m_ofn.Flags` has the `OFN_ALLOWMULTISELECT` flag set, this string contains a sequence of null-terminated strings, with the first string being the directory path of the file group selected, followed by the names of all files selected by the user. For this reason, use the [GetStartPosition](../vs140/CFileDialog--GetStartPosition.md) and [GetNextPathName](../vs140/CFileDialog--GetNextPathName.md) member functions to retrieve the next file name in the list.  
  
## Example  
 See the example for [CFileDialog::DoModal](../vs140/CFileDialog--DoModal.md).  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CFileDialog Class](../vs140/CFileDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFileDialog::GetPathName](../vs140/CFileDialog--GetPathName.md)   
 [CFileDialog::GetFileName](../vs140/CFileDialog--GetFileName.md)   
 [CFileDialog::GetFileExt](../vs140/CFileDialog--GetFileExt.md)   
 [GetFileTitle](http://msdn.microsoft.com/library/windows/desktop/ms646924)