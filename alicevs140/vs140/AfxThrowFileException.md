---
title: "AfxThrowFileException"
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
ms.assetid: 714be79a-81ce-43fe-8d19-d07186e95d02
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AfxThrowFileException
Throws a file exception.  
  
## Syntax  
  
```  
  
      void AfxThrowFileException(  
   int cause,  
   LONG lOsError = -1,  
   LPCTSTR lpszFileName = NULL   
);   
```  
  
#### Parameters  
 `cause`  
 Specifies an integer that indicates the reason for the exception. For a list of the possible values, see [CFileException::m_cause](../vs140/CFileException--m_cause.md).  
  
 `lOsError`  
 Contains the operating-system error number (if available) that states the reason for the exception. See your operating-system manual for a listing of error codes.  
  
 `lpszFileName`  
 Points to a string containing the name of the file that caused the exception (if available).  
  
## Remarks  
 You are responsible for determining the cause based on the operating-system error code.  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [CFileException::ThrowOsError](../vs140/CFileException--ThrowOsError.md)   
 [THROW](../vs140/THROW--MFC-.md)