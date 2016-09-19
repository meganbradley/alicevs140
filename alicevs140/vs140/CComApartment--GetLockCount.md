---
title: "CComApartment::GetLockCount"
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
ms.assetid: b0908f5d-3157-49bf-9227-5abb49eee139
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComApartment::GetLockCount
Returns the thread's current lock count.  
  
## Syntax  
  
```  
  
LONG GetLockCount( );  
  
```  
  
## Return Value  
 The lock count on the thread.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CComApartment Class](../vs140/CComApartment-Class.md)   
 [CComApartment::Lock](../vs140/CComApartment--Lock.md)   
 [CComApartment::Unlock](../vs140/CComApartment--Unlock.md)   
 [CComApartment::m_nLockCnt](../vs140/CComApartment--m_nLockCnt.md)