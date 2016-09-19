---
title: "CFileFind::IsCompressed"
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
ms.assetid: 79938fca-6448-4079-b6c7-15e2d1927e51
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFileFind::IsCompressed
Call this member function to determine if the found file is compressed.  
  
## Syntax  
  
```  
  
BOOL IsCompressed( ) const;  
  
```  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 A compressed file is marked with FILE_ATTRIBUTE_COMPRESSED, a file attribute identified in the [WIN32_FIND_DATA](http://msdn.microsoft.com/library/windows/desktop/aa365740) structure. For a file, this attribute indicates that all of the data in the file is compressed. For a directory, this attribute indicates that compression is the default for newly created files and subdirectories.  
  
 You must call [FindNextFile](../vs140/CFileFind--FindNextFile.md) at least once before calling `IsCompressed`.  
  
 See the member function [MatchesMask](../vs140/CFileFind--MatchesMask.md) for a complete list of file attributes.  
  
## Example  
 See the example for [CFileFind::GetLength](../vs140/CFileFind--GetLength.md).  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CFileFind Class](../vs140/CFileFind-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)