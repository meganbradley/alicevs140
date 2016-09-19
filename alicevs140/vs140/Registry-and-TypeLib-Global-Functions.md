---
title: "Registry and TypeLib Global Functions"
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
ms.assetid: d58b8a4e-975c-4417-8b34-d3c847f679b3
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Registry and TypeLib Global Functions
These functions provide support for loading and registering a type library.  
  
> [!IMPORTANT]
>  The functions listed in the following tables cannot be used in applications that execute in the [!INCLUDE[wrt](../vs140/includes/wrt_md.md)].  
  
|||  
|-|-|  
|[AtlRegisterTypeLib](../vs140/AtlRegisterTypeLib.md)|This function is called to register a type library.|  
|[AtlUnRegisterTypeLib](../vs140/AtlUnRegisterTypeLib.md)|This function is called to unregister a type library|  
|[AtlLoadTypeLib](../vs140/AtlLoadTypeLib.md)|This function is called to load a type library.|  
|[AtlUpdateRegistryFromResourceD](../vs140/AtlUpdateRegistryFromResourceD.md)|This function is called to update the registry from the supplied resource.|  
|[RegistryDataExchange](../vs140/RegistryDataExchange.md)|This function is called to read from, or write to, the system registry. Called by the [Registry Data Exchange Macros](../vs140/Registry-Data-Exchange-Macros.md).|  
  
 These functions control which node in the registry the program uses to store information.  
  
|||  
|-|-|  
|[AtlGetPerUserRegistration](../vs140/AtlGetPerUserRegistration.md)|Retrieves whether the application redirects registry access to the **HKEY_CURRENT_USER** (**HKCU**) node.|  
|[AtlSetPerUserRegistration](../vs140/AtlSetPerUserRegistration.md)|Sets whether the application redirects registry access to the **HKEY_CURRENT_USER** (**HKCU**) node.|  
  
## See Also  
 [Functions](../vs140/ATL-Functions.md)