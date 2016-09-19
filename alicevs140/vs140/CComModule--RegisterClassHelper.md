---
title: "CComModule::RegisterClassHelper"
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
ms.assetid: 2ca9827e-5e86-4e8c-9cf3-00d6cc06f5c5
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComModule::RegisterClassHelper
As of ATL 7.0, `CComModule` is obsolete: see [ATL Module Classes](../vs140/ATL-Module-Classes.md) for more details.  
  
## Syntax  
  
```  
  
      ATL_DEPRECATED HRESULT RegisterClassHelper(  
   const CLSID& clsid,  
   LPCTSTR lpszProgID,  
   LPCTSTR lpszVerIndProgID,  
   UINT nDescID,  
   DWORD dwFlags   
);  
```  
  
#### Parameters  
 `clsid`  
 [in] The CLSID of the object to be registered.  
  
 `lpszProgID`  
 [in] The ProgID associated with the object.  
  
 `lpszVerIndProgID`  
 [in] The version-independent ProgID associated with the object.  
  
 `nDescID`  
 [in] The identifier of a string resource for the object's description.  
  
 `dwFlags`  
 [in] Specifies the threading model to enter in the registry. Possible values are **THREADFLAGS_APARTMENT**, **THREADFLAGS_BOTH**, or **AUTPRXFLAG**.  
  
## Return Value  
 A standard HRESULT value.  
  
## Remarks  
 Enters an object's standard class registration in the system registry.  
  
 The [UpdateRegistryClass](../vs140/CComModule--UpdateRegistryClass.md) method calls `RegisterClassHelper`.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CComModule Class](../vs140/CComModule-Class.md)   
 [CComModule::UnregisterClassHelper](../vs140/CComModule--UnregisterClassHelper.md)