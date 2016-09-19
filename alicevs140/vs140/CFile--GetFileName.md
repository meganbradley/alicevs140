---
title: "CFile::GetFileName"
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
ms.assetid: fc9cc012-0297-4f06-8c91-b9c99f231d6f
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFile::GetFileName
Call this member function to retrieve the name of a specified file.  
  
## Syntax  
  
```  
  
virtual CString GetFileName( ) const;  
  
```  
  
## Return Value  
 The name of the file.  
  
## Remarks  
 For example, when you call `GetFileName` to generate a message to the user about the file `c:\windows\write\myfile.wri`, the filename, `myfile.wri`, is returned.  
  
 To return the entire path of the file, including the name, call [GetFilePath](../vs140/CFile--GetFilePath.md). To return the title of the file (`myfile`), call [GetFileTitle](../vs140/CFile--GetFileTitle.md).  
  
## Example  
 This code fragment opens the SYSTEM.INI file in your WINDOWS directory. If found, the example will print out the name and path and title, as shown under Output:  
  
 [!CODE [NVC_MFCFiles#6](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCFiles#6)]  
  
## Output  
 `Path is : "C:\WINDOWS\SYSTEM.INI"`  
  
 `Name is : "SYSTEM.INI"`  
  
 `Title is: "System"`  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CFile Class](../vs140/CFile-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFile::GetFilePath](../vs140/CFile--GetFilePath.md)   
 [CFile::GetFileTitle](../vs140/CFile--GetFileTitle.md)