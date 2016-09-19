---
title: "AfxThrowArchiveException"
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
ms.topic: article
ms.assetid: 56b9db3e-d139-45c9-924a-4e95d133fca5
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AfxThrowArchiveException
Throws an archive exception.  
  
## Syntax  
  
```  
  
      void AfxThrowArchiveException(  
   int cause,  
   LPCTSTR lpszArchiveName   
);   
```  
  
#### Parameters  
 `cause`  
 Specifies an integer that indicates the reason for the exception. For a list of the possible values, see [CArchiveException::m_cause](../vs140/CArchiveException--m_cause.md).  
  
 `lpszArchiveName`  
 Points to a string containing the name of the `CArchive` object that caused the exception (if available).  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [CArchiveException Class](../vs140/CArchiveException-Class.md)   
 [THROW](../vs140/THROW--MFC-.md)