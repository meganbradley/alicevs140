---
title: "CFileFind::GetFileURL"
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
ms.assetid: dc498259-5d1f-4687-b9d0-964e1673e49a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFileFind::GetFileURL
Call this member function to retrieve the specified URL.  
  
## Syntax  
  
```  
  
virtual CString GetFileURL( ) const;  
  
```  
  
## Return Value  
 The complete URL.  
  
## Remarks  
 You must call [FindNextFile](../vs140/CFileFind--FindNextFile.md) at least once before calling `GetFileURL`.  
  
 `GetFileURL` is similar to the member function [GetFilePath](../vs140/CFileFind--GetFilePath.md), except that it returns the URL in the form `file://path`. For example, calling `GetFileURL` to get the complete URL for `myfile.txt` returns the URL `file://c:\myhtml\myfile.txt`.  
  
## Example  
 See the example for [CFileFind::GetFileName](../vs140/CFileFind--GetFileName.md).  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CFileFind Class](../vs140/CFileFind-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFileFind::FindFile](../vs140/CFileFind--FindFile.md)