---
title: "CComCritSecLock::Unlock"
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
ms.assetid: 7298728d-cab7-4bb2-8c50-689c286e727a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComCritSecLock::Unlock
Call this method to unlock the critical section object.  
  
## Syntax  
  
```  
  
void Unlock( ) throw( );  
  
```  
  
## Remarks  
 If the object is already unlocked, an ASSERT error will occur in debug builds.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CComCritSecLock Class](../vs140/CComCritSecLock-Class.md)   
 [CComCritSecLock::Lock](../vs140/CComCritSecLock--Lock.md)