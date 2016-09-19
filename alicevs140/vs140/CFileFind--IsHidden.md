---
title: "CFileFind::IsHidden"
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
ms.assetid: d53ba7ff-e69a-40c0-99b1-4ca02014e2c2
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFileFind::IsHidden
Call this member function to determine if the found file is hidden.  
  
## Syntax  
  
```  
  
BOOL IsHidden( ) const;  
  
```  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 Hidden files, which are marked with FILE_ATTRIBUTE_HIDDEN, a file attribute identified in the [WIN32_FIND_DATA](http://msdn.microsoft.com/library/windows/desktop/aa365740) structure. A hidden file is not included in an ordinary directory listing.  
  
 You must call [FindNextFile](../vs140/CFileFind--FindNextFile.md) at least once before calling `IsHidden`.  
  
 See the member function [MatchesMask](../vs140/CFileFind--MatchesMask.md) for a complete list of file attributes.  
  
## Example  
 See the example for [CFileFind::GetLength](../vs140/CFileFind--GetLength.md).  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CFileFind Class](../vs140/CFileFind-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)