---
title: "CHeapPtrBase::operator -&gt;"
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
ms.assetid: e2d981d9-88cb-4004-aad4-7e23045e5c30
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHeapPtrBase::operator -&gt;
The pointer-to-member operator.  
  
## Syntax  
  
```  
  
T* operator ->( ) const throw( );  
  
```  
  
## Return Value  
 Returns the value of the [CHeapPtrBase::m_pData](../vs140/CHeapPtrBase--m_pData.md) member variable.  
  
## Remarks  
 Use this operator to call a method in a class pointed to by the `CHeapPtrBase` object. In debug builds, an assertion failure will occur if the `CHeapPtrBase` points to NULL.  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CHeapPtrBase Class](../vs140/CHeapPtrBase-Class.md)