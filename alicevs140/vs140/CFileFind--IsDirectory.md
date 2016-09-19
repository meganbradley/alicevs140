---
title: "CFileFind::IsDirectory"
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
ms.assetid: f1911844-bbcf-4442-b59b-6dcc4121611b
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFileFind::IsDirectory
Call this member function to determine if the found file is a directory.  
  
## Syntax  
  
```  
  
BOOL IsDirectory( ) const;  
  
```  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 A file that is a directory is marked with FILE_ATTRIBUTE_DIRECTORY a file attribute identified in the [WIN32_FIND_DATA](http://msdn.microsoft.com/library/windows/desktop/aa365740) structure.  
  
 You must call [FindNextFile](../vs140/CFileFind--FindNextFile.md) at least once before calling `IsDirectory`.  
  
 See the member function [MatchesMask](../vs140/CFileFind--MatchesMask.md) for a complete list of file attributes.  
  
## Example  
 This small program recurses every directory on the C:\ drive and prints the name of the directory.  
  
 [!CODE [NVC_MFCFiles#34](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCFiles#34)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CFileFind Class](../vs140/CFileFind-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)