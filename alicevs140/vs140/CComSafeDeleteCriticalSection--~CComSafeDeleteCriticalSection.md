---
title: "CComSafeDeleteCriticalSection::~CComSafeDeleteCriticalSection"
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
ms.assetid: 7accebc9-9249-4289-9626-19ba98ffa19c
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComSafeDeleteCriticalSection::~CComSafeDeleteCriticalSection
The destructor.  
  
## Syntax  
  
```  
  
~CComSafeDeleteCriticalSection() throw();  
  
```  
  
## Remarks  
 Releases the internal **CRITICAL_SECTION** object from memory if the [m_bInitialized](../vs140/CComSafeDeleteCriticalSection--m_bInitialized.md) data member is set to **true**.  
  
## Requirements  
 **Header:** atlcore.h  
  
## See Also  
 [CComSafeDeleteCriticalSection Class](../vs140/CComSafeDeleteCriticalSection-Class.md)