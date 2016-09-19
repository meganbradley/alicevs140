---
title: "CComFakeCriticalSection Class"
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
ms.assetid: a4811b97-96bb-493b-ab9f-62822aeddb10
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComFakeCriticalSection Class
This class provides the same methods as [CComCriticalSection](../vs140/CComCriticalSection-Class.md) but does not provide a critical section.  
  
## Syntax  
  
```  
  
class CComFakeCriticalSection  
  
```  
  
## Members  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CComFakeCriticalSection::Init](../vs140/CComFakeCriticalSection--Init.md)|Does nothing since there is no critical section.|  
|[CComFakeCriticalSection::Lock](../vs140/CComFakeCriticalSection--Lock.md)|Does nothing since there is no critical section.|  
|[CComFakeCriticalSection::Term](../vs140/CComFakeCriticalSection--Term.md)|Does nothing since there is no critical section.|  
|[CComFakeCriticalSection::Unlock](../vs140/CComFakeCriticalSection--Unlock.md)|Does nothing since there is no critical section.|  
  
## Remarks  
 `CComFakeCriticalSection` mirrors the methods found in [CComCriticalSection](../vs140/CComCriticalSection-Class.md). However, `CComFakeCriticalSection` does not provide a critical section; therefore, its methods do nothing.  
  
 Typically, you use `CComFakeCriticalSection` through a `typedef` name, either `AutoCriticalSection` or `CriticalSection`. When using [CComSingleThreadModel](../vs140/CComSingleThreadModel-Class.md) or [CComMultiThreadModelNoCS](../vs140/CComMultiThreadModelNoCS-Class.md), both of these `typedef` names reference `CComFakeCriticalSection`. When using [CComMultiThreadModel](../vs140/CComMultiThreadModel-Class.md), they reference [CComAutoCriticalSection](../vs140/CComAutoCriticalSection-Class.md) and `CComCriticalSection`, respectively.  
  
## Requirements  
 **Header:** atlcore.h  
  
##  <a name="ccomfakecriticalsection__init"></a>  CComFakeCriticalSection::Init  
 Does nothing since there is no critical section.  
  
```  
  
HRESULT Init( ) throw( );  
  
```  
  
### Return Value  
 Returns S_OK.  
  
##  <a name="ccomfakecriticalsection__lock"></a>  CComFakeCriticalSection::Lock  
 Does nothing since there is no critical section.  
  
```  
  
HRESULT Lock( ) throw( );  
  
```  
  
### Return Value  
 Returns S_OK.  
  
##  <a name="ccomfakecriticalsection__term"></a>  CComFakeCriticalSection::Term  
 Does nothing since there is no critical section.  
  
```  
  
HRESULT Term( ) throw( );  
  
```  
  
### Return Value  
 Returns S_OK.  
  
##  <a name="ccomfakecriticalsection__unlock"></a>  CComFakeCriticalSection::Unlock  
 Does nothing since there is no critical section.  
  
```  
  
HRESULT Unlock( ) throw( );  
  
```  
  
### Return Value  
 Returns S_OK.  
  
## See Also  
 [Class Overview](../vs140/ATL-Class-Overview.md)