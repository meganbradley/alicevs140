---
title: "CAutoPtr::Attach"
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
ms.assetid: 35f7e389-5841-43b7-83b8-56a7110d6211
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAutoPtr::Attach
Call this method to take ownership of an existing pointer.  
  
## Syntax  
  
```  
  
      void Attach(  
   T* p   
) throw( );  
```  
  
#### Parameters  
 `p`  
 The `CAutoPtr` object will take ownership of this pointer.  
  
## Remarks  
 When a `CAutoPtr` object takes ownership of a pointer, it will automatically delete the pointer and any allocated data when it goes out of scope. If [CAutoPtr::Detach](../vs140/CAutoPtr--Detach.md) is called, the programmer is again given responsibility for freeing any allocated resources.  
  
 In debug builds, an assertion failure will occur if the [CAutoPtr::m_p](../vs140/CAutoPtr--m_p.md) data member currently points to an existing value; that is, it is not equal to NULL.  
  
## Example  
 See the example in the [CAutoPtr Overview](../vs140/CAutoPtr-Class.md).  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CAutoPtr Class](../vs140/CAutoPtr-Class.md)   
 [CAutoPtr::Detach](../vs140/CAutoPtr--Detach.md)   
 [CAutoPtr::operator =](../vs140/CAutoPtr--operator-=.md)