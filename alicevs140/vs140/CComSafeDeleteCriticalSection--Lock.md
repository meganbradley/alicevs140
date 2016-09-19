---
title: "CComSafeDeleteCriticalSection::Lock"
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
ms.assetid: 6b2fb65b-8e30-4b1e-8dea-13965cbaca0b
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComSafeDeleteCriticalSection::Lock
Calls the base class implementation of [Lock](../vs140/CComCriticalSection--Lock.md).  
  
## Syntax  
  
```  
  
HRESULT Lock();  
  
```  
  
## Return Value  
 Returns the result of [CComCriticalSection::Lock](../vs140/CComCriticalSection--Lock.md).  
  
## Remarks  
 This method assumes the [m_bInitialized](../vs140/CComSafeDeleteCriticalSection--m_bInitialized.md) data member is set to **true** upon entry. An assertion is generated in Debug builds if this condidtion is not met.  
  
 For more information on the behavior of the function, refer to [CComCriticalSection::Lock](../vs140/CComCriticalSection--Lock.md).  
  
## Requirements  
 **Header:** atlcore.h  
  
## See Also  
 [CComSafeDeleteCriticalSection Class](../vs140/CComSafeDeleteCriticalSection-Class.md)