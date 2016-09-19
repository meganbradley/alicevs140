---
title: "CFileException::ThrowErrno"
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
ms.assetid: e0088d8a-89ed-4ad8-8128-edc456cfb33d
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFileException::ThrowErrno
Constructs a `CFileException` object corresponding to a given `nErrno` value, then throws the exception.  
  
## Syntax  
  
```  
  
      static void PASCAL ThrowErrno(  
   int nErrno,   
   LPCTSTR lpszFileName = NULL  
);  
```  
  
#### Parameters  
 `nErrno`  
 An integer error code as defined in the run-time include file ERRNO.H.  
  
 `lpszFileName`  
 A pointer to the string containing the name of the file that caused the exception, if available.  
  
## Example  
 [!CODE [NVC_MFCFiles#28](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCFiles#28)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CFileException Class](../vs140/CFileException-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFileException::ThrowOsError](../vs140/CFileException--ThrowOsError.md)