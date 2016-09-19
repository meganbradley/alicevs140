---
title: "DECLARE_REGISTRY"
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
ms.assetid: 89b8949b-5c27-4a9c-8a51-ad276bba3a54
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DECLARE_REGISTRY
Enters the standard class registration into the system registry or removes it from the system registry.  
  
## Syntax  
  
```  
  
      DECLARE_REGISTRY(   
   class,   
   pid,   
   vpid,   
   nid,   
   flags    
)  
```  
  
#### Parameters  
 `class`  
 [in] Included for backward compatibility.  
  
 `pid`  
 [in] An `LPCTSTR` that is a version-specific program identifier.  
  
 *vpid*  
 [in] An `LPCTSTR` that is a version-independent program identifier.  
  
 *nid*  
 [in] A **UINT** that is an index of the resource string in the registry to use as the description of the program.  
  
 `flags`  
 [in] A `DWORD` containing the program's threading model in the registry. Must be one of the following values: **THREADFLAGS_APARTMENT**, **THREADFLAGS_BOTH**, or **AUTPRXFLAG**.  
  
## Remarks  
 The standard registration consists of the CLSID, program ID, version-independent program ID, description string, and thread model.  
  
 When you create an object or control using the ATL Add Class Wizard, the wizard automatically implements script-based registry support and adds the [DECLARE_REGISTRY_RESOURCEID](../vs140/DECLARE_REGISTRY_RESOURCEID.md) macro to your files. If you do not want script-based registry support, you need to replace this macro with `DECLARE_REGISTRY`. `DECLARE_REGISTRY` only inserts the five basic keys described above into the registry. You must manually write code to insert other keys into the registry.  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [Registry Macros](../vs140/Registry-Macros.md)   
 [Macros](../vs140/ATL-Macros.md)   
 [DECLARE_REGISTRY_RESOURCE](../vs140/DECLARE_REGISTRY_RESOURCE.md)