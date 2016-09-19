---
title: "DECLARE_REGISTRY_RESOURCE"
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
ms.assetid: 7ac11498-8ee2-4156-8df2-7076f7ddda8b
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DECLARE_REGISTRY_RESOURCE
Gets the named resource containing the registry file and runs the script to either enter objects into the system registry or remove them from the system registry.  
  
## Syntax  
  
```  
  
      DECLARE_REGISTRY_RESOURCE(   
   x    
)  
```  
  
#### Parameters  
 *x*  
 [in] String identifier of your resource.  
  
## Remarks  
 When you create an object or control using the ATL Project Wizard, the wizard will automatically implement script-based registry support and add the [DECLARE_REGISTRY_RESOURCEID](../vs140/DECLARE_REGISTRY_RESOURCEID.md) macro, which is similar to `DECLARE_REGISTRY_RESOURCE`, to your files.  
  
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
 [_ATL_STATIC_REGISTRY](../vs140/_ATL_STATIC_REGISTRY.md)