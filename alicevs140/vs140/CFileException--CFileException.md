---
title: "CFileException::CFileException"
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
ms.assetid: 2b159e0f-7fbe-4d81-8842-8b1500073182
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFileException::CFileException
Constructs a `CFileException` object that stores the cause code and the operating-system code in the object.  
  
## Syntax  
  
```  
  
      CFileException(   
   int cause = CFileException::none,    
   LONG lOsError = -1,    
   LPCTSTR lpszArchiveName = NULL   
);  
```  
  
#### Parameters  
 `cause`  
 An enumerated type variable that indicates the reason for the exception. See [CFileException::m_cause](../vs140/CFileException--m_cause.md) for a list of the possible values.  
  
 `lOsError`  
 An operating-system-specific reason for the exception, if available. The `lOsError` parameter provides more information than `cause` does.  
  
 `lpszArchiveName`  
 Points to a string containing the name of the `CFile` object causing the exception.  
  
## Remarks  
 Do not use this constructor directly, but rather call the global function [AfxThrowFileException](../vs140/AfxThrowFileException.md).  
  
> [!NOTE]
>  The variable `lOsError` applies only to `CFile` and `CStdioFile` objects. The `CMemFile` class does not handle this error code.  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CFileException Class](../vs140/CFileException-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [AfxThrowFileException](../vs140/AfxThrowFileException.md)