---
title: "IRunnableObjectImpl::LockRunning"
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
ms.assetid: e9ba77de-ccd0-4ecc-85d5-8e44887a022f
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IRunnableObjectImpl::LockRunning
Locks the control into the running state.  
  
## Syntax  
  
```  
  
      HRESULT LockRunning(  
   BOOL fLock,  
   BOOL fLastUnlockCloses   
);  
```  
  
## Return Value  
 The ATL implementation returns `S_OK`.  
  
## Remarks  
 See [IRunnableObject::LockRunning](http://msdn.microsoft.com/library/windows/desktop/ms693361) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IRunnableObjectImpl Class](../vs140/IRunnableObjectImpl-Class.md)