---
title: "CComClassFactory::LockServer"
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
ms.assetid: b9f38d05-02e3-4e43-bad2-a26d66ad5cf3
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComClassFactory::LockServer
Increments and decrements the module lock count by calling **_Module::Lock** and **_Module::Unlock**, respectively.  
  
## Syntax  
  
```  
  
      STDMETHOD(LockServer)(  
   BOOL fLock   
);  
```  
  
#### Parameters  
 `fLock`  
 [in] If **TRUE**, the lock count is incremented; otherwise, the lock count is decremented.  
  
## Return Value  
 A standard `HRESULT` value.  
  
## Remarks  
 **_Module** refers to the global instance of [CComModule](../vs140/CComModule-Class.md) or a class derived from it.  
  
 Calling `LockServer` allows a client to hold onto a class factory so that multiple objects can be created quickly.  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [CComClassFactory Class](../vs140/CComClassFactory-Class.md)