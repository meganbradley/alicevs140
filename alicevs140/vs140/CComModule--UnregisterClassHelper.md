---
title: "CComModule::UnregisterClassHelper"
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
ms.assetid: 07b98ad2-3d6d-4be4-8d5d-82279f0eef07
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComModule::UnregisterClassHelper
As of ATL 7.0, `CComModule` is obsolete: see [ATL Module Classes](../vs140/ATL-Module-Classes.md) for more details.  
  
## Syntax  
  
```  
  
      ATL_DEPRECATED HRESULT UnregisterClassHelper(  
   const CLSID& clsid,  
   LPCTSTR lpszProgID,  
   LPCTSTR lpszVerIndProgID   
);  
```  
  
#### Parameters  
 `clsid`  
 [in] The CLSID of the object to be unregistered.  
  
 `lpszProgID`  
 [in] The ProgID associated with the object.  
  
 `lpszVerIndProgID`  
 [in] The version-independent ProgID associated with the object.  
  
## Return Value  
 A standard HRESULT value.  
  
## Remarks  
 Removes an object's standard class registration from the system registry.  
  
 The [UpdateRegistryClass](../vs140/CComModule--UpdateRegistryClass.md) method calls `UnregisterClassHelper`.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CComModule Class](../vs140/CComModule-Class.md)   
 [CComModule::RegisterClassHelper](../vs140/CComModule--RegisterClassHelper.md)