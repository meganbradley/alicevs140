---
title: "CFileFind::GetRoot"
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
ms.assetid: 32283524-efcb-493d-a925-a9675d77f153
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFileFind::GetRoot
Call this member function to get the root of the found file.  
  
## Syntax  
  
```  
  
virtual CString GetRoot( ) const;  
  
```  
  
## Return Value  
 The root of the active search.  
  
## Remarks  
 You must call [FindNextFile](../vs140/CFileFind--FindNextFile.md) at least once before calling `GetRoot`.  
  
 This member function returns the drive specifier and path name used to start a search. For example, calling [FindFile](../vs140/CFileFind--FindFile.md) with `*.dat` results in `GetRoot` returning an empty string. Passing a path, such as `c:\windows\system\*.dll`, to **FindFile** results `GetRoot` returning `c:\windows\system\`.  
  
## Example  
 See the example for [CFileFind::GetFileName](../vs140/CFileFind--GetFileName.md).  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CFileFind Class](../vs140/CFileFind-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)