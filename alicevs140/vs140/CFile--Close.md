---
title: "CFile::Close"
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
ms.assetid: ba12bcef-bf23-49ae-8871-4f4fb0ea98c1
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFile::Close
Closes the file associated with this object and makes the file unavailable for reading or writing.  
  
## Syntax  
  
```  
  
virtual void Close( );  
```  
  
## Remarks  
 If you have not closed the file before destroying the object, the destructor closes it for you.  
  
 If you used **new** to allocate the `CFile` object on the heap, then you must delete it after closing the file. **Close** sets `m_hFile` to `CFile::hFileNull`.  
  
## Example  
 See the example for [CFile::CFile](../vs140/CFile--CFile.md).  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CFile Class](../vs140/CFile-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFile::Open](../vs140/CFile--Open.md)