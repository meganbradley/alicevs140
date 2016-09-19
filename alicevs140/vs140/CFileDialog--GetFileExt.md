---
title: "CFileDialog::GetFileExt"
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
ms.assetid: 374512fe-5d0b-4180-a713-c8bff68d980a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFileDialog::GetFileExt
Call this function to retrieve the extension of the filename entered into the dialog box.  
  
## Syntax  
  
```  
  
CString GetFileExt( ) const;  
```  
  
## Return Value  
 The extension of the filename.  
  
## Remarks  
 For example, if the name of the file entered is DATA.TXT, `GetFileExt` returns "TXT".  
  
 If `m_ofn.Flags` has the `OFN_ALLOWMULTISELECT` flag set, this string contains a sequence of null-terminated strings, with the first string being the directory path of the file group selected, followed by the names of all files selected by the user. To retrieve file pathnames, use the [GetStartPosition](../vs140/CFileDialog--GetStartPosition.md) and [GetNextPathName](../vs140/CFileDialog--GetNextPathName.md) member functions.  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CFileDialog Class](../vs140/CFileDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFileDialog::GetPathName](../vs140/CFileDialog--GetPathName.md)   
 [CFileDialog::GetFileName](../vs140/CFileDialog--GetFileName.md)   
 [CFileDialog::GetFileTitle](../vs140/CFileDialog--GetFileTitle.md)