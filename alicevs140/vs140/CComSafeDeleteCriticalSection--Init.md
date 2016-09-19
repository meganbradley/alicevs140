---
title: "CComSafeDeleteCriticalSection::Init"
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
ms.assetid: 63aab6ef-4f9f-4bc6-9916-f1100722ba7c
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComSafeDeleteCriticalSection::Init
Calls the base class implementation of [Init](../vs140/CComCriticalSection--Init.md) and sets [m_bInitialized](../vs140/CComSafeDeleteCriticalSection--m_bInitialized.md) to **true** if successful.  
  
## Syntax  
  
```  
  
HRESULT Init() throw();  
  
```  
  
## Return Value  
 Returns the result of [CComCriticalSection::Init](../vs140/CComCriticalSection--Init.md).  
  
## Requirements  
 **Header:** atlcore.h  
  
## See Also  
 [CComSafeDeleteCriticalSection Class](../vs140/CComSafeDeleteCriticalSection-Class.md)