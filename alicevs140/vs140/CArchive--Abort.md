---
title: "CArchive::Abort"
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
ms.assetid: ae91832b-8d96-406e-a858-98a02cea7e3a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CArchive::Abort
Call this function to close the archive without throwing an exception.  
  
## Syntax  
  
```  
  
void Abort ( );  
```  
  
## Remarks  
 The **CArchive** destructor will normally call **Close**, which will flush any data that has not been saved to the associated `CFile` object. This can cause exceptions.  
  
 When catching these exceptions, it is a good idea to use **Abort**, so that destructing the `CArchive` object doesn't cause further exceptions. When handling exceptions, `CArchive::Abort` will not throw an exception on failures because, unlike [CArchive::Close](../vs140/CArchive--Close.md), **Abort** ignores failures.  
  
 If you used **new** to allocate the `CArchive` object on the heap, then you must delete it after closing the file.  
  
## Example  
 See the example for [CArchive::WriteClass](../vs140/CArchive--WriteClass.md).  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CArchive Class](../vs140/CArchive-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CArchive::Close](../vs140/CArchive--Close.md)   
 [CFile::Close](../vs140/CFile--Close.md)