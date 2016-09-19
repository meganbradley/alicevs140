---
title: "CComAutoThreadModule::CreateInstance"
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
ms.assetid: 20c3a1ef-300e-4fcd-b189-c11c62265924
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComAutoThreadModule::CreateInstance
As of ATL 7.0, `CComAutoThreadModule` is obsolete: see [ATL Module Classes](../vs140/ATL-Module-Classes.md) for more details.  
  
## Syntax  
  
```  
  
      HRESULT CreateInstance(  
   void* pfnCreateInstance,  
   REFIID riid,  
   void** ppvObj   
);  
```  
  
#### Parameters  
 *pfnCreateInstance*  
 [in] A pointer to a creator function.  
  
 `riid`  
 [in] The IID of the requested interface.  
  
 `ppvObj`  
 [out] A pointer to the interface pointer identified by `riid`. If the object does not support this interface, `ppvObj` is set to NULL.  
  
## Return Value  
 A standard HRESULT value.  
  
## Remarks  
 Selects a thread and then creates an object in the associated apartment.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CComAutoThreadModule Class](../vs140/CComAutoThreadModule-Class.md)