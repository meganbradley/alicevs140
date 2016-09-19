---
title: "CComModule::UpdateRegistryFromResourceS"
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
ms.assetid: 5e0ec2cf-182d-4798-95b1-4eb85462468b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComModule::UpdateRegistryFromResourceS
As of ATL 7.0, `CComModule` is obsolete: see [ATL Module Classes](../vs140/ATL-Module-Classes.md) for more details.  
  
## Syntax  
  
```  
  
      virtual HRESULT UpdateRegistryFromResourceS(  
   LPCTSTR lpszRes,  
   BOOL bRegister,  
   struct _ATL_REGMAP_ENTRY* pMapEntries = NULL   
) throw( );  
virtual HRESULT UpdateRegistryFromResourceS(  
   UINT nResID,  
   BOOL bRegister,  
   struct _ATL_REGMAP_ENTRY* pMapEntries = NULL   
) throw( );  
```  
  
#### Parameters  
 `lpszRes`  
 [in] A resource name.  
  
 `nResID`  
 [in] A resource ID.  
  
 `bRegister`  
 [in] Indicates whether the resource script should be registered.  
  
 `pMapEntries`  
 [in] A pointer to the replacement map storing values associated with the script's replaceable parameters. ATL automatically uses `%MODULE%`. To use additional replaceable parameters, see the Remarks for details. Otherwise, use the **NULL** default value.  
  
## Return Value  
 A standard HRESULT value.  
  
## Remarks  
 Similar to [UpdateRegistryFromResourceD](../vs140/CComModule--UpdateRegistryFromResourceD.md) except `UpdateRegistryFromResourceS` creates a static link to the ATL Registry Component (Registrar).  
  
 `UpdateRegistryFromResourceS` will be invoked automatically when your object map is processed, provided you add `#define _ATL_STATIC_REGISTRY` to your stdafx.h.  
  
> [!NOTE]
>  To substitute replacement values at run time, do not specify the [DECLARE_REGISTRY_RESOURCE](../vs140/DECLARE_REGISTRY_RESOURCE.md) or [DECLARE_REGISTRY_RESOURCEID](../vs140/DECLARE_REGISTRY_RESOURCEID.md) macro. Instead, create an array of **_ATL_REGMAP_ENTRIES** structures, where each entry contains a variable placeholder paired with a value to replace the placeholder at run time. Then call `UpdateRegistryFromResourceS`, passing the array for the `pMapEntries` parameter. This adds all the replacement values in the **_ATL_REGMAP_ENTRIES** structures to the Registrar's replacement map.  
  
 For more information about replaceable parameters and scripting, see the article [The ATL Registry Component (Registrar)](../vs140/ATL-Registry-Component--Registrar-.md).  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CComModule Class](../vs140/CComModule-Class.md)