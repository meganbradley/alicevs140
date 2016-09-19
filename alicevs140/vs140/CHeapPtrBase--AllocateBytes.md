---
title: "CHeapPtrBase::AllocateBytes"
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
ms.assetid: f4dcadad-c91b-477e-9b91-415418647459
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHeapPtrBase::AllocateBytes
Call this method to allocate memory.  
  
## Syntax  
  
```  
  
      bool AllocateBytes(  
   size_t nBytes   
) throw( );  
```  
  
#### Parameters  
 `nBytes`  
 The number of bytes of memory to allocate.  
  
## Return Value  
 Returns true if the memory is successfully allocated, false otherwise.  
  
## Remarks  
 In debug builds, an assertion failure will occur if the [CHeapPtrBase::m_pData](../vs140/CHeapPtrBase--m_pData.md) member variable currently points to an existing value; that is, it is not equal to NULL.  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CHeapPtrBase Class](../vs140/CHeapPtrBase-Class.md)   
 [CHeapPtrBase::Free](../vs140/CHeapPtrBase--Free.md)   
 [CHeapPtrBase::ReallocateBytes](../vs140/CHeapPtrBase--ReallocateBytes.md)