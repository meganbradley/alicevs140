---
title: "CFileFind::GetFileTitle"
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
ms.assetid: 1504cac0-13fc-4d33-81ee-75350bd88f67
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFileFind::GetFileTitle
Call this member function to get the title of the found file.  
  
## Syntax  
  
```  
  
virtual CString GetFileTitle( ) const;  
  
```  
  
## Return Value  
 The title of the file.  
  
## Remarks  
 You must call [FindNextFile](../vs140/CFileFind--FindNextFile.md) at least once before calling `GetFileTitle`.  
  
 `GetFileTitle` is one of three `CFileFind` member functions that return some form of the file name. The following list describes the three and how they vary:  
  
-   [GetFileName](../vs140/CFileFind--GetFileName.md) returns the file name, including the extension. For example, calling `GetFileName` to generate a user message about the file `c:\myhtml\myfile.txt` returns the file name `myfile.txt`.  
  
-   [GetFilePath](../vs140/CFileFind--GetFilePath.md) returns the entire path for the file. For example, calling `GetFilePath` to generate a user message about the file `c:\myhtml\myfile.txt` returns the file path `c:\myhtml\myfile.txt`.  
  
-   `GetFileTitle` returns the file name, excluding the file extension. For example, calling `GetFileTitle` to generate a user message about the file `c:\myhtml\myfile.txt` returns the file title `myfile`.  
  
## Example  
 See the example for [CFileFind::GetFileName](../vs140/CFileFind--GetFileName.md).  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CFileFind Class](../vs140/CFileFind-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFileFind::FindFile](../vs140/CFileFind--FindFile.md)