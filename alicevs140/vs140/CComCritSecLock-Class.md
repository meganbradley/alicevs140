---
title: "CComCritSecLock Class"
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
ms.assetid: 223152a1-86c3-4ef9-89a7-f455fe791b0e
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComCritSecLock Class
This class provides methods for locking and unlocking a critical section object.  
  
## Syntax  
  
```  
  
template<  
      class  TLock  
   > class CComCritSecLock  
  
```  
  
#### Parameters  
 *TLock*  
 The object to be locked and unlocked.  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CComCritSecLock::CComCritSecLock](../vs140/CComCritSecLock--CComCritSecLock.md)|The constructor.|  
|[CComCritSecLock::~CComCritSecLock](../vs140/CComCritSecLock--~CComCritSecLock.md)|The destructor.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CComCritSecLock::Lock](../vs140/CComCritSecLock--Lock.md)|Call this method to lock the critical section object.|  
|[CComCritSecLock::Unlock](../vs140/CComCritSecLock--Unlock.md)|Call this method to unlock the critical section object.|  
  
## Remarks  
 Use this class to lock and unlock objects in a safer way than with the [CComCriticalSection Class](../vs140/CComCriticalSection-Class.md) or [CComAutoCriticalSection Class](../vs140/CComAutoCriticalSection-Class.md).  
  
## Requirements  
 **Header:** atlbase.h  
  
##  <a name="ccomcritseclock__ccomcritseclock"></a>  CComCritSecLock::CComCritSecLock  
 The constructor.  
  
```  
  
CComCritSecLock(  
      TLock&  cs,  
      bool  bInitialLock  
    = true   
   );  
  
```  
  
### Parameters  
 *cs*  
 The critical section object.  
  
 `bInitialLock`  
 The initial lock state:                                 **true** means locked.  
  
### Remarks  
 Initializes the critical section object.  
  
##  <a name="ccomcritseclock___dtorccomcritseclock"></a>  CComCritSecLock::~CComCritSecLock  
 The destructor.  
  
```  
  
~CComCritSecLock( ) throw( );  
  
```  
  
### Remarks  
 Unlocks the critical section object.  
  
##  <a name="ccomcritseclock__lock"></a>  CComCritSecLock::Lock  
 Call this method to lock the critical section object.  
  
```  
  
HRESULT Lock( ) throw( );  
  
```  
  
### Return Value  
 Returns S_OK if the object has successfully been locked, or an error HRESULT on failure.  
  
### Remarks  
 If the object is already locked, an ASSERT error will occur in debug builds.  
  
##  <a name="ccomcritseclock__unlock"></a>  CComCritSecLock::Unlock  
 Call this method to unlock the critical section object.  
  
```  
  
void Unlock( ) throw( );  
  
```  
  
### Remarks  
 If the object is already unlocked, an ASSERT error will occur in debug builds.  
  
## See Also  
 [CComCriticalSection Class](../vs140/CComCriticalSection-Class.md)   
 [CComAutoCriticalSection Class](../vs140/CComAutoCriticalSection-Class.md)