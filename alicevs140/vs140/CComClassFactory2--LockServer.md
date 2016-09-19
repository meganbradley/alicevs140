---
title: "CComClassFactory2::LockServer"
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
ms.assetid: 894e2e37-1822-42f6-868f-71b095c237b5
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComClassFactory2::LockServer
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
  
 Calling `LockServer` allows a client to hold onto a class factory so that multiple objects can be quickly created.  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [CComClassFactory2 Class](../vs140/CComClassFactory2-Class.md)