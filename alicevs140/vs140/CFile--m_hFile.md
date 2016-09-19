---
title: "CFile::m_hFile"
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
ms.assetid: ca7a5dda-34fc-498f-871b-cf885fe6a33f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFile::m_hFile
Contains the operating-system file handle for an open file.  
  
## Syntax  
  
```  
  
HANDLE m_hFile;  
  
```  
  
## Remarks  
 `m_hFile` is a public variable of type **UINT**. It contains `CFile::hFileNull` (an operating-system-independent empty file indicator) if the handle has not been assigned.  
  
 Use of `m_hFile` is not recommended because the member's meaning depends on the derived class. `m_hFile` is made a public member for convenience in supporting nonpolymorphic use of the class.  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CFile Class](../vs140/CFile-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)