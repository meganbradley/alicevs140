---
title: "CHeapPtrBase::ReallocateBytes"
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
ms.assetid: 431aad7d-47db-45d6-9d75-d12364392ecf
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHeapPtrBase::ReallocateBytes
Call this method to reallocate memory.  
  
## Syntax  
  
```  
  
      bool ReallocateBytes(  
   size_t nBytes   
) throw( );  
```  
  
#### Parameters  
 `nBytes`  
 The new amount of memory to allocate, in bytes.  
  
## Return Value  
 Returns true if the memory is successfully allocated, false otherwise.  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CHeapPtrBase Class](../vs140/CHeapPtrBase-Class.md)   
 [CHeapPtrBase::AllocateBytes](../vs140/CHeapPtrBase--AllocateBytes.md)   
 [CHeapPtrBase::Free](../vs140/CHeapPtrBase--Free.md)