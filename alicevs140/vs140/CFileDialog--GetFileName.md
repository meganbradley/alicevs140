---
title: "CFileDialog::GetFileName"
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
ms.assetid: 69179eec-f628-4f46-a6dc-627a7614f799
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFileDialog::GetFileName
Call this function to retrieve the name of the filename entered in the dialog box.  
  
## Syntax  
  
```  
  
CString GetFileName( ) const;  
```  
  
## Return Value  
 The name of the file.  
  
## Remarks  
 The name of the file includes both the prefix and the extension. For example, `GetFileName` will return "TEXT.DAT" for the file C:\FILES\TEXT.DAT.  
  
 If `m_ofn.Flags` has the `OFN_ALLOWMULTISELECT` flag set, you should call [GetStartPosition](../vs140/CFileDialog--GetStartPosition.md) and [GetNextPathName](../vs140/CFileDialog--GetNextPathName.md) to retrieve a file pathname.  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CFileDialog Class](../vs140/CFileDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFileDialog::GetPathName](../vs140/CFileDialog--GetPathName.md)   
 [CFileDialog::GetStartPosition](../vs140/CFileDialog--GetStartPosition.md)   
 [CFileDialog::GetFileTitle](../vs140/CFileDialog--GetFileTitle.md)