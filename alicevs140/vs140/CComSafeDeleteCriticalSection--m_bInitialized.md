---
title: "CComSafeDeleteCriticalSection::m_bInitialized"
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
ms.assetid: 8bf6998c-1419-41ca-9aab-1d5b64c3280d
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComSafeDeleteCriticalSection::m_bInitialized
Flags whether the internal **CRITICAL_SECTION** object has been initialized.  
  
## Syntax  
  
```  
  
bool m_bInitialized;  
  
```  
  
## Remarks  
 The **m_bInitialized** data member is used to track validity of the underlying **CRITICAL_SECTION** object associated with the [CComSafeDeleteCriticalSection](../vs140/CComSafeDeleteCriticalSection-Class.md) class. The underlying **CRITICAL_SECTION** object will not be attempted to be released from memory if this flag is not set to **true**.  
  
## Requirements  
 **Header:** atlcore.h  
  
## See Also  
 [CComSafeDeleteCriticalSection Class](../vs140/CComSafeDeleteCriticalSection-Class.md)   
 [CComSafeDeleteCriticalSection::Lock](../vs140/CComSafeDeleteCriticalSection--Lock.md)   
 [CComSafeDeleteCriticalSection::Init](../vs140/CComSafeDeleteCriticalSection--Init.md)   
 [CComSafeDeleteCriticalSection::Term](../vs140/CComSafeDeleteCriticalSection--Term.md)