---
title: "CArchiveException::CArchiveException"
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
ms.assetid: 0ea53a3e-9a80-4468-a989-138aaf520e05
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CArchiveException::CArchiveException
Constructs a `CArchiveException` object, storing the value of `cause` in the object.  
  
## Syntax  
  
```  
  
      CArchiveException(  
   int cause = CArchiveException::none,  
   LPCTSTR lpszArchiveName = NULL  
);  
```  
  
#### Parameters  
 `cause`  
 An enumerated type variable that indicates the reason for the exception. For a list of the enumerators, see the [m_cause](../vs140/CArchiveException--m_cause.md) data member.  
  
 `lpszArchiveName`  
 Points to a string containing the name of the `CArchive` object causing the exception.  
  
## Remarks  
 You can create a `CArchiveException` object on the heap and throw it yourself or let the global function [AfxThrowArchiveException](../vs140/AfxThrowArchiveException.md) handle it for you.  
  
 Do not use this constructor directly; instead, call the global function `AfxThrowArchiveException`.  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CArchiveException Class](../vs140/CArchiveException-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)