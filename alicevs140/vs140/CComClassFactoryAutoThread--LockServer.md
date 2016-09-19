---
title: "CComClassFactoryAutoThread::LockServer"
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
ms.assetid: 7115192a-6e3a-4172-bfc5-7e101c8359de
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComClassFactoryAutoThread::LockServer
Increments and decrements the module lock count by calling **_Module::Lock** and **_Module::Unlock**, respectively.  
  
## Syntax  
  
```  
  
      STDMETHODIMP LockServer(  
   BOOL fLock   
);  
```  
  
#### Parameters  
 `fLock`  
 [in] If **TRUE**, the lock count is incremented; otherwise, the lock count is decremented.  
  
## Return Value  
 A standard `HRESULT` value.  
  
## Remarks  
 When using `CComClassFactoryAutoThread`, **_Module** typically refers to the global instance of [CComAutoThreadModule](../vs140/CComAutoThreadModule-Class.md).  
  
 Calling `LockServer` allows a client to hold onto a class factory so that multiple objects can be quickly created.  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [CComClassFactoryAutoThread Class](../vs140/CComClassFactoryAutoThread-Class.md)   
 [CComAutoThreadModule::Lock](../vs140/CComAutoThreadModule--Lock.md)   
 [CComAutoThreadModule::Unlock](../vs140/CComAutoThreadModule--Unlock.md)