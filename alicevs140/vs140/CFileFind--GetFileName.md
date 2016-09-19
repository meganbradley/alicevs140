---
title: "CFileFind::GetFileName"
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
ms.assetid: eb2c08dd-e1d3-4361-8c3b-8bf5d62758ec
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFileFind::GetFileName
Call this member function to get the name of the found file.  
  
## Syntax  
  
```  
  
virtual CString GetFileName( ) const;  
  
```  
  
## Return Value  
 The name of the most-recently-found file.  
  
## Remarks  
 You must call [FindNextFile](../vs140/CFileFind--FindNextFile.md) at least once before calling GetFileName.  
  
 `GetFileName` is one of three `CFileFind` member functions that return some form of the file name. The following list describes the three and how they vary:  
  
-   `GetFileName` returns the file name, including the extension. For example, calling `GetFileName` to generate a user message about the file `c:\myhtml\myfile.txt` returns the file name `myfile.txt`.  
  
-   [GetFilePath](../vs140/CFileFind--GetFilePath.md) returns the entire path for the file. For example, calling `GetFilePath` to generate a user message about the file `c:\myhtml\myfile.txt` returns the file path `c:\myhtml\myfile.txt`.  
  
-   [GetFileTitle](../vs140/CFileFind--GetFileTitle.md) returns the file name, excluding the file extension. For example, calling `GetFileTitle` to generate a user message about the file `c:\myhtml\myfile.txt` returns the file title `myfile`.  
  
## Example  
 [!CODE [NVC_MFCFiles#32](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCFiles#32)]  
  
## Output  
 Assumes that the file C:\WINDOWS\SYSTEM.INI exists:  
  
 `Root of C:\WINDOWS\SYSTEM.INI is C:\WINDOWS`  
  
 `Title of C:\WINDOWS\SYSTEM.INI is SYSTEM`  
  
 `Path of C:\WINDOWS\SYSTEM.INI is C:\WINDOWS\SYSTEM.INI`  
  
 `URL of C:\WINDOWS\SYSTEM.INI is file://C:\WINDOWS\SYSTEM.INI`  
  
 `Name of C:\WINDOWS\SYSTEM.INI is SYSTEM.INI`  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CFileFind Class](../vs140/CFileFind-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFileFind::FindFile](../vs140/CFileFind--FindFile.md)