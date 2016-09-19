---
title: "CComCriticalSection::Unlock"
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
ms.assetid: 3b74ccf6-db0c-4f9f-a7df-69d979fb04a6
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComCriticalSection::Unlock
Calls the Win32 function [LeaveCriticalSection](http://msdn.microsoft.com/library/windows/desktop/ms684169), which releases ownership of the critical section object contained in the [m_sec](../vs140/CComCriticalSection--m_sec.md) data member.  
  
## Syntax  
  
```  
  
HRESULT Unlock( ) throw( );  
  
```  
  
## Return Value  
 Returns `S_OK`.  
  
## Remarks  
 To first obtain ownership, the thread must call the [Lock](../vs140/CComCriticalSection--Lock.md) method. Each call to `Lock` requires a corresponding call to `Unlock` to release ownership of the critical section.  
  
## Requirements  
 **Header:** atlcore.h  
  
## See Also  
 [CComCriticalSection Class](../vs140/CComCriticalSection-Class.md)