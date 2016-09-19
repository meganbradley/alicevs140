---
title: "CHeapPtrBase::Attach"
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
ms.assetid: 346877e4-4890-4a2f-b283-8ffd92bae5c5
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHeapPtrBase::Attach
Call this method to take ownership of an existing pointer.  
  
## Syntax  
  
```  
  
      void Attach(  
   T* pData   
) throw( );  
```  
  
#### Parameters  
 `pData`  
 The `CHeapPtrBase` object will take ownership of this pointer.  
  
## Remarks  
 When a `CHeapPtrBase` object takes ownership of a pointer, it will automatically delete the pointer and any allocated data when it goes out of scope.  
  
 In debug builds, an assertion failure will occur if the [CHeapPtrBase::m_pData](../vs140/CHeapPtrBase--m_pData.md) member variable currently points to an existing value; that is, it is not equal to NULL.  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CHeapPtrBase Class](../vs140/CHeapPtrBase-Class.md)   
 [CHeapPtrBase::Detach](../vs140/CHeapPtrBase--Detach.md)