---
title: "CComModule::UpdateRegistryClass"
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
ms.assetid: 46001300-844f-4f74-8a4d-f13fdfec8a88
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComModule::UpdateRegistryClass
As of ATL 7.0, `CComModule` is obsolete: see [ATL Module Classes](../vs140/ATL-Module-Classes.md) for more details.  
  
## Syntax  
  
```  
  
      ATL_DEPRECATED HRESULT UpdateRegistryClass(  
   const CLSID& clsid,  
   LPCTSTR lpszProgID,  
   LPCTSTR lpszVerIndProgID,  
   UINT nDescID,  
   DWORD dwFlags,  
   BOOL bRegister   
);  
ATL_DEPRECATED HRESULT UpdateRegistryClass(  
   const CLSID& clsid,  
   LPCTSTR lpszProgID,  
   LPCTSTR lpszVerIndProgID,  
   LPCTSTR szDesc,  
   DWORD dwFlags,  
   BOOL bRegister   
);  
```  
  
#### Parameters  
 `clsid`  
 The CLSID of the object to be registered or unregistered.  
  
 `lpszProgID`  
 The ProgID associated with the object.  
  
 `lpszVerIndProgID`  
 The version-independent ProgID associated with the object.  
  
 `nDescID`  
 The identifier of the string resource for the object's description.  
  
 `szDesc`  
 A string containing the object's description.  
  
 `dwFlags`  
 Specifies the threading model to enter in the registry. Possible values are **THREADFLAGS_APARTMENT**, **THREADFLAGS_BOTH**, or **AUTPRXFLAG**.  
  
 `bRegister`  
 Indicates whether the object should be registered.  
  
## Return Value  
 A standard HRESULT value.  
  
## Remarks  
 If `bRegister` is **TRUE**, this method enters the object's standard class registration in the system registry.  
  
 If `bRegister` is **FALSE**, it removes the object's registration.  
  
 Depending on the value of `bRegister`, `UpdateRegistryClass` calls either [RegisterClassHelper](../vs140/CComModule--RegisterClassHelper.md) or [UnregisterClassHelper](../vs140/CComModule--UnregisterClassHelper.md).  
  
 By specifying the [DECLARE_REGISTRY](../vs140/DECLARE_REGISTRY.md) macro, `UpdateRegistryClass` will be invoked automatically when your object map is processed.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CComModule Class](../vs140/CComModule-Class.md)