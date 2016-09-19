---
title: "CDocument::ReleaseFile"
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
ms.assetid: e3a598e1-4027-44e5-b41d-bea2f1ae5040
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDocument::ReleaseFile
This member function is called by the framework to release a file, making it available for use by other applications.  
  
## Syntax  
  
```  
  
      virtual void ReleaseFile(  
   CFile* pFile,  
   BOOL bAbort   
);  
```  
  
#### Parameters  
 `pFile`  
 A pointer to the CFile object to be released.  
  
 `bAbort`  
 Specifies whether the file is to be released by using either `CFile::Close` or `CFile::Abort`. **FALSE** if the file is to be released using [CFile::Close](../vs140/CFile--Close.md); **TRUE** if the file is to be released using [CFile::Abort](../vs140/CFile--Abort.md).  
  
## Remarks  
 If `bAbort` is **TRUE**, `ReleaseFile` calls `CFile::Abort`, and the file is released. `CFile::Abort` will not throw an exception.  
  
 If `bAbort` is **FALSE**, `ReleaseFile` calls `CFile::Close` and the file is released.  
  
 Override this member function to require an action by the user before the file is released.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDocument Class](../vs140/CDocument-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDocTemplate Class](../vs140/CDocTemplate-Class.md)   
 [CFile::Close](../vs140/CFile--Close.md)   
 [CFile::Abort](../vs140/CFile--Abort.md)