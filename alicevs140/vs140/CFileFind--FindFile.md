---
title: "CFileFind::FindFile"
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
ms.assetid: 4e59db30-9d52-4fc8-9ef0-d817040e1ef1
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFileFind::FindFile
Call this member function to open a file search.  
  
## Syntax  
  
```  
  
      virtual BOOL FindFile(  
   LPCTSTR pstrName = NULL,  
   DWORD dwUnused = 0   
);  
```  
  
#### Parameters  
 `pstrName`  
 A pointer to a string containing the name of the file to find. If you pass **NULL** for `pstrName`, **FindFile** does a wildcard (*.\*) search.  
  
 *dwUnused*  
 Reserved to make **FindFile** polymorphic with derived classes. Must be 0.  
  
## Return Value  
 Nonzero if successful; otherwise 0. To get extended error information, call the Win32 function [GetLastError](http://msdn.microsoft.com/library/windows/desktop/ms679360).  
  
## Remarks  
 After calling **FindFile** to begin the file search, call [FindNextFile](../vs140/CFileFind--FindNextFile.md) to retrieve subsequent files. You must call `FindNextFile` at least once before calling any of the following attribute member functions:  
  
-   [GetCreationTime](../vs140/CFileFind--GetCreationTime.md)  
  
-   [GetFileName](../vs140/CFileFind--GetFileName.md)  
  
-   [GetFileTitle](../vs140/CFileFind--GetFileTitle.md)  
  
-   [GetFilePath](../vs140/CFileFind--GetFilePath.md)  
  
-   [GetFileURL](../vs140/CFileFind--GetFileURL.md)  
  
-   [GetLastAccessTime](../vs140/CFileFind--GetLastAccessTime.md)  
  
-   [GetLastWriteTime](../vs140/CFileFind--GetLastWriteTime.md)  
  
-   [GetLength](../vs140/CFileFind--GetLength.md)  
  
-   [GetRoot](../vs140/CFileFind--GetRoot.md)  
  
-   [IsArchived](../vs140/CFileFind--IsArchived.md)  
  
-   [IsCompressed](../vs140/CFileFind--IsCompressed.md)  
  
-   [IsDirectory](../vs140/CFileFind--IsDirectory.md)  
  
-   [IsDots](../vs140/CFileFind--IsDots.md)  
  
-   [IsHidden](../vs140/CFileFind--IsHidden.md)  
  
-   [IsNormal](../vs140/CFileFind--IsNormal.md)  
  
-   [IsReadOnly](../vs140/CFileFind--IsReadOnly.md)  
  
-   [IsSystem](../vs140/CFileFind--IsSystem.md)  
  
-   [IsTemporary](../vs140/CFileFind--IsTemporary.md)  
  
-   [MatchesMask](../vs140/CFileFind--MatchesMask.md)  
  
## Example  
 See the example for [CFileFind::IsDirectory](../vs140/CFileFind--IsDirectory.md).  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CFileFind Class](../vs140/CFileFind-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFileFind::FindNextFile](../vs140/CFileFind--FindNextFile.md)