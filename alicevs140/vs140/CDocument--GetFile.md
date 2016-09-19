---
title: "CDocument::GetFile"
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
ms.assetid: c48a894e-7024-42fc-ba5a-10a5cf5ebbb2
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDocument::GetFile
Call this member function to get a pointer to a `CFile` object.  
  
## Syntax  
  
```  
  
      virtual CFile* GetFile(  
   LPCTSTR lpszFileName,  
   UINT nOpenFlags,  
   CFileException* pError   
);  
```  
  
#### Parameters  
 `lpszFileName`  
 A string that is the path to the desired file. The path may be relative or absolute.  
  
 `pError`  
 A pointer to an existing file-exception object that indicates the completion status of the operation.  
  
 `nOpenFlags`  
 Sharing and access mode. Specifies the action to take when opening the file. You can combine options listed in the CFile constructor [CFile::CFile](../vs140/CFile--CFile.md) by using the bitwise OR (&#124;) operator. One access permission and one share option are required; the **modeCreate** and **modeNoInherit** modes are optional.  
  
## Return Value  
 A pointer to a `CFile` object.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDocument Class](../vs140/CDocument-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDocTemplate Class](../vs140/CDocTemplate-Class.md)