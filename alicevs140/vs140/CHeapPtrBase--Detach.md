---
title: "CHeapPtrBase::Detach"
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
ms.assetid: 12d8a930-da71-4865-9bea-0a2605a6e8ce
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHeapPtrBase::Detach
Call this method to release ownership of a pointer.  
  
## Syntax  
  
```  
  
T* Detach( ) throw( );  
  
```  
  
## Return Value  
 Returns a copy of the pointer.  
  
## Remarks  
 Releases ownership of a pointer, sets the [CHeapPtrBase::m_pData](../vs140/CHeapPtrBase--m_pData.md) member variable to NULL, and returns a copy of the pointer.  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CHeapPtrBase Class](../vs140/CHeapPtrBase-Class.md)   
 [CHeapPtrBase::Attach](../vs140/CHeapPtrBase--Attach.md)