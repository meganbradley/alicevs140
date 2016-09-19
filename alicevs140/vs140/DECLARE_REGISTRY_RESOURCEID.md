---
title: "DECLARE_REGISTRY_RESOURCEID"
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
ms.assetid: 65bf3576-5396-416e-ba48-e14b3236c49b
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DECLARE_REGISTRY_RESOURCEID
Same as [DECLARE_REGISTRY_RESOURCE](../vs140/DECLARE_REGISTRY_RESOURCE.md) except that it uses a wizard-generated **UINT** to identify the resource, rather than a string name.  
  
## Syntax  
  
```  
  
      DECLARE_REGISTRY_RESOURCEID(   
   x    
)  
```  
  
#### Parameters  
 *x*  
 [in] Wizard-generated identifier of your resource.  
  
## Remarks  
 When you create an object or control using the ATL Project Wizard, the wizard will automatically implement script-based registry support and add the `DECLARE_REGISTRY_RESOURCEID` macro to your files.  
  
 You can statically link with the ATL Registry Component (Registrar) for optimized registry access. To statically link to the Registrar code, add the following line to your stdafx.h file:  
  
 [!CODE [NVC_ATL_COM#56](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_COM#56)]  
  
 If you want ATL to substitute replacement values at run time, do not specify the `DECLARE_REGISTRY_RESOURCE` or `DECLARE_REGISTRY_RESOURCEID` macro. Instead, create an array of **_ATL_REGMAP_ENTRIES** structures, where each entry contains a variable placeholder paired with a value to replace the placeholder at run time. Then call [CAtlModule::UpdateRegistryFromResourceD](../vs140/CAtlModule--UpdateRegistryFromResourceD.md) or [CAtlModule::UpdateRegistryFromResourceS](../vs140/CAtlModule--UpdateRegistryFromResourceS.md), passing the array. This adds all of the replacement values in the **_ATL_REGMAP_ENTRIES** structures to the Registrar's replacement map.  
  
 For more information about replaceable parameters and scripting, see the article [The ATL Registry Component (Registrar)](../vs140/ATL-Registry-Component--Registrar-.md).  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [Registry Macros](../vs140/Registry-Macros.md)   
 [Macros](../vs140/ATL-Macros.md)   
 [DECLARE_REGISTRY](../vs140/DECLARE_REGISTRY.md)   
 [DECLARE_REGISTRY_RESOURCE](../vs140/DECLARE_REGISTRY_RESOURCE.md)