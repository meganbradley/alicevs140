---
title: "CFileException::ErrnoToException"
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
ms.assetid: 0aa0b602-2a47-4c5a-841d-8b9be744ff99
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFileException::ErrnoToException
Converts a given run-time library error value to a `CFileException` enumerated error value.  
  
## Syntax  
  
```  
  
      static int PASCAL ErrnoToException(  
   int nErrno   
);  
```  
  
#### Parameters  
 `nErrno`  
 An integer error code as defined in the run-time include file ERRNO.H.  
  
## Return Value  
 Enumerated value that corresponds to a given run-time library error value.  
  
## Remarks  
 See [CFileException::m_cause](../vs140/CFileException--m_cause.md) for a list of the possible enumerated values.  
  
## Example  
 [!CODE [NVC_MFCFiles#26](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCFiles#26)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CFileException Class](../vs140/CFileException-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFileException::OsErrorToException](../vs140/CFileException--OsErrorToException.md)