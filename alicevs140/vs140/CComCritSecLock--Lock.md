---
title: "CComCritSecLock::Lock"
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
ms.assetid: d247c378-7d7a-49c0-8236-436d765c3a04
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComCritSecLock::Lock
Call this method to lock the critical section object.  
  
## Syntax  
  
```  
  
HRESULT Lock( ) throw( );  
  
```  
  
## Return Value  
 Returns S_OK if the object has successfully been locked, or an error HRESULT on failure.  
  
## Remarks  
 If the object is already locked, an ASSERT error will occur in debug builds.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CComCritSecLock Class](../vs140/CComCritSecLock-Class.md)   
 [CComCritSecLock::Unlock](../vs140/CComCritSecLock--Unlock.md)