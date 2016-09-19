---
title: "CAutoVectorPtr::Allocate"
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
ms.assetid: 82b74821-d8d3-4afe-b021-a3a4b3e8f94a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAutoVectorPtr::Allocate
Call this method to allocate the memory required by the array of objects pointed to by `CAutoVectorPtr`.  
  
## Syntax  
  
```  
  
      bool Allocate(  
   size_t nElements   
) throw( );  
```  
  
#### Parameters  
 `nElements`  
 The number of elements in the array.  
  
## Return Value  
 Returns true if the memory is successfully allocated, false on failure.  
  
## Remarks  
 In debug builds, an assertion failure will occur if the [CAutoVectorPtr::m_p](../vs140/CAutoVectorPtr--m_p.md) member variable currently points to an existing value; that is, it is not equal to NULL.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CAutoVectorPtr Class](../vs140/CAutoVectorPtr-Class.md)