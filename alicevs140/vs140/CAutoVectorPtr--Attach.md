---
title: "CAutoVectorPtr::Attach"
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
ms.assetid: 53320770-fa1e-47c1-b932-16f5761b211d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAutoVectorPtr::Attach
Call this method to take ownership of an existing pointer.  
  
## Syntax  
  
```  
  
      void Attach(  
   T* p   
) throw( );  
```  
  
#### Parameters  
 `p`  
 The `CAutoVectorPtr` object will take ownership of this pointer.  
  
## Remarks  
 When a `CAutoVectorPtr` object takes ownership of a pointer, it will automatically delete the pointer and any allocated data when it goes out of scope. If [CAutoVectorPtr::Detach](../vs140/CAutoVectorPtr--Detach.md) is called, the programmer is again given responsibility for freeing any allocated resources.  
  
 In debug builds, an assertion failure will occur if the [CAutoVectorPtr::m_p](../vs140/CAutoVectorPtr--m_p.md) member variable currently points to an existing value; that is, it is not equal to NULL.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CAutoVectorPtr Class](../vs140/CAutoVectorPtr-Class.md)   
 [CAutoVectorPtr::Detach](../vs140/CAutoVectorPtr--Detach.md)   
 [CAutoVectorPtr::operator =](../vs140/CAutoVectorPtr--operator-=.md)