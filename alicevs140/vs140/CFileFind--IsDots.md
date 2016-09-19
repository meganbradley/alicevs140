---
title: "CFileFind::IsDots"
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
ms.assetid: 92fe97f2-c0f7-4102-9894-d8e223537ca8
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFileFind::IsDots
Call this member function to test for the current directory and parent directory markers while iterating through files.  
  
## Syntax  
  
```  
  
virtual BOOL IsDots( ) const;  
  
```  
  
## Return Value  
 Nonzero if the found file has the name "." or "..", which indicates that the found file is actually a directory. Otherwise 0.  
  
## Remarks  
 You must call [FindNextFile](../vs140/CFileFind--FindNextFile.md) at least once before calling `IsDots`.  
  
## Example  
 See the example for [CFileFind::IsDirectory](../vs140/CFileFind--IsDirectory.md).  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CFileFind Class](../vs140/CFileFind-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFileFind::IsDirectory](../vs140/CFileFind--IsDirectory.md)