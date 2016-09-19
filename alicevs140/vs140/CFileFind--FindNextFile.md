---
title: "CFileFind::FindNextFile"
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
ms.assetid: 5fc32d17-8d3c-4ba6-baf0-0a94e3178603
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFileFind::FindNextFile
Call this member function to continue a file search from a previous call to [FindFile](../vs140/CFileFind--FindFile.md).  
  
## Syntax  
  
```  
  
virtual BOOL FindNextFile( );  
  
```  
  
## Return Value  
 Nonzero if there are more files; zero if the file found is the last one in the directory or if an error occurred. To get extended error information, call the Win32 function [GetLastError](http://msdn.microsoft.com/library/windows/desktop/ms679360). If the file found is the last file in the directory, or if no matching files can be found, the `GetLastError` function returns ERROR_NO_MORE_FILES.  
  
## Remarks  
 You must call `FindNextFile` at least once before calling any of the following attribute member functions:  
  
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
  
 `FindNextFile` wraps the Win32 function [FindNextFile](http://msdn.microsoft.com/library/windows/desktop/aa364428).  
  
## Example  
 See the example for [CFileFind::IsDirectory](../vs140/CFileFind--IsDirectory.md).  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CFileFind Class](../vs140/CFileFind-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)