---
title: "CFileDialog::GetPathName"
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
ms.assetid: 6d7c0439-d125-4e23-9d99-2f660efb5503
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFileDialog::GetPathName
Call this function to retrieve the full path of the file entered in the dialog box.  
  
## Syntax  
  
```  
  
CString GetPathName( ) const;  
```  
  
## Return Value  
 The full path of the file.  
  
## Remarks  
 The path of the filename includes the file's title plus the entire directory path. For example, `GetPathName` will return "C:\FILES\TEXT.DAT" for the file C:\FILES\TEXT.DAT.  
  
 If `m_ofn.Flags` has the `OFN_ALLOWMULTISELECT` flag set, this string contains a sequence of null-teminated strings, with the first string being the directory path of the file group selected, followed by the names of all files selected by the user. For this reason, use the [GetStartPosition](../vs140/CFileDialog--GetStartPosition.md) and [GetNextPathName](../vs140/CFileDialog--GetNextPathName.md) member functions to retrieve the next file name in the list.  
  
## Example  
 See the example for [CFileDialog::DoModal](../vs140/CFileDialog--DoModal.md).  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CFileDialog Class](../vs140/CFileDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFileDialog::GetFileName](../vs140/CFileDialog--GetFileName.md)   
 [CFileDialog::GetFileExt](../vs140/CFileDialog--GetFileExt.md)   
 [CFileDialog::GetFileTitle](../vs140/CFileDialog--GetFileTitle.md)