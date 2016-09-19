---
title: "CComApartment::Unlock"
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
ms.assetid: 56569cbf-50a4-4faf-b10b-c19a61d4987f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComApartment::Unlock
Decrements the thread's lock count.  
  
## Syntax  
  
```  
  
LONG Unlock( );  
  
```  
  
## Return Value  
 A value that may be useful for diagnostics or testing.  
  
## Remarks  
 Called by [CComAutoThreadModule::Unlock](../vs140/CComAutoThreadModule--Lock.md).  
  
 The lock count on the thread is used for statistical purposes.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CComApartment Class](../vs140/CComApartment-Class.md)   
 [CComApartment::Lock](../vs140/CComApartment--Lock.md)   
 [CComApartment::GetLockCount](../vs140/CComApartment--GetLockCount.md)   
 [CComApartment::m_nLockCnt](../vs140/CComApartment--m_nLockCnt.md)