---
title: "CFileFind::GetLength"
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
ms.assetid: bb82cd97-6174-449e-8ecc-6afa8ee4da26
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFileFind::GetLength
Call this member function to get the length of the found file, in bytes.  
  
## Syntax  
  
```  
  
ULONGLONG GetLength( ) const;  
  
```  
  
## Return Value  
 The length of the found file, in bytes.  
  
## Remarks  
 You must call [FindNextFile](../vs140/CFileFind--FindNextFile.md) at least once before calling `GetLength`.  
  
 `GetLength` uses the Win32 structure [WIN32_FIND_DATA](http://msdn.microsoft.com/library/windows/desktop/aa365740) to get and return the value of the file size, in bytes.  
  
> [!NOTE]
>  As of MFC 7.0, `GetLength` supports 64-bit integer types. Previously existing code built with this newer version of the library may result in truncation warnings.  
  
## Example  
 [!CODE [NVC_MFCFiles#33](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCFiles#33)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CFileFind Class](../vs140/CFileFind-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)