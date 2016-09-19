---
title: "CAtlModule::UpdateRegistryFromResourceD"
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
ms.assetid: 15f0ac82-1313-43ac-9043-f11408b274c4
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlModule::UpdateRegistryFromResourceD
Runs the script contained in a specified resource to register or unregister an object.  
  
## Syntax  
  
```  
  
      HRESULT WINAPI UpdateRegistryFromResourceD(  
   UINT nResID,  
   BOOL bRegister,  
   struct _ATL_REGMAP_ENTRY* pMapEntries = NULL   
) throw( );  
HRESULT WINAPI UpdateRegistryFromResourceD(  
   LPCTSTR lpszRes,  
   BOOL bRegister,  
   struct _ATL_REGMAP_ENTRY* pMapEntries = NULL   
) throw( );  
```  
  
#### Parameters  
 `lpszRes`  
 A resource name.  
  
 `nResID`  
 A resource ID.  
  
 `bRegister`  
 **TRUE** if the object should be registered; **FALSE** otherwise.  
  
 `pMapEntries`  
 A pointer to the replacement map storing values associated with the script's replaceable parameters. ATL automatically uses %MODULE%. To use additional replaceable parameters, see [CAtlModule::AddCommonRGSReplacements](../vs140/CAtlModule--AddCommonRGSReplacements.md). Otherwise, use the **NULL** default value.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 Runs the script contained in the resource specified by *lpszRes or nResID*. If `bRegister` is **TRUE**, this method registers the object in the system registry; otherwise it removes the object from the registry.  
  
 To statically link to the ATL Registry Component (Registrar), see [CAtlModule::UpdateRegistryFromResourceS](../vs140/CAtlModule--UpdateRegistryFromResourceS.md).  
  
 This method calls [CAtlModule::UpdateRegistryFromResourceDHelper](../vs140/CAtlModule--UpdateRegistryFromResourceDHelper.md).  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CAtlModule Class](../vs140/CAtlModule-Class.md)