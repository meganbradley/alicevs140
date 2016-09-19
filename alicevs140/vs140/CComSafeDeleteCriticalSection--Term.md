---
title: "CComSafeDeleteCriticalSection::Term"
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
ms.assetid: 818b08bb-20e0-4f20-89c2-ea0ed38dcd76
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComSafeDeleteCriticalSection::Term
Calls the base class implementation of [CComCriticalSection::Term](../vs140/CComCriticalSection--Term.md) if the internal **CRITICAL_SECTION** object is valid.  
  
## Syntax  
  
```  
  
HRESULT Term() throw();  
  
```  
  
## Return Value  
 Returns the result of [CComCriticalSection::Term](../vs140/CComCriticalSection--Term.md), or **S_OK** if [m_bInitialized](../vs140/CComSafeDeleteCriticalSection--m_bInitialized.md) was set to **false** upon entry.  
  
## Remarks  
 It is safe to call this method even if the internal **CRITICAL_SECTION** object is not valid. The destructor of this class calls this method if the [m_bInitialized](../vs140/CComSafeDeleteCriticalSection--m_bInitialized.md) data member is set to **true**.  
  
## Requirements  
 **Header:** atlcore.h  
  
## See Also  
 [CComSafeDeleteCriticalSection Class](../vs140/CComSafeDeleteCriticalSection-Class.md)