---
title: "CFile::Abort"
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
ms.assetid: 76f54d52-5b12-40c7-adad-a5c18d4919cf
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFile::Abort
Closes the file associated with this object and makes the file unavailable for reading or writing.  
  
## Syntax  
  
```  
  
virtual void Abort( );  
```  
  
## Remarks  
 If you have not closed the file before destroying the object, the destructor closes it for you.  
  
 When handling exceptions, `CFile::Abort` differs from `CFile::Close` in two important ways. First, the **Abort** function will not throw an exception on failures because failures are ignored by **Abort**. Second, **Abort** will not **ASSERT** if the file has not been opened or was closed previously.  
  
 If you used **new** to allocate the `CFile` object on the heap, then you must delete it after closing the file. **Abort** sets `m_hFile` to `CFile::hFileNull`.  
  
## Example  
 [!CODE [NVC_MFCFiles#5](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCFiles#5)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CFile Class](../vs140/CFile-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFile::Close](../vs140/CFile--Close.md)   
 [CFile::Open](../vs140/CFile--Open.md)