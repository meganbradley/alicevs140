---
title: "TerminateMap Function"
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
ms.assetid: 1c314a61-da5d-49bb-ac44-c34ee3c23b66
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# TerminateMap Function
Supports the WRL infrastructure and is not intended to be used directly from your code.  
  
## Syntax  
  
```  
inline bool TerminateMap(  
   _In_ ModuleBase *module,   
   _In_opt_z_ const wchar_t *serverName,   
    bool forceTerminate) throw()  
```  
  
## Parameters  
 `module`  
 A [module](../vs140/Module-Class.md).  
  
 `serverName`  
 The name of a subset of class factories in the module specified by parameter `module`.  
  
 `forceTerminate`  
 `true` to terminate the class factories regardless of they are active; `false` to not terminate the class factories if any factory is active.  
  
## Return Value  
 `true` if all class factories were terminated; otherwise, `false`.  
  
## Remarks  
 Shuts down the class factories in the specified module.  
  
## Requirements  
 **Header:** module.h  
  
 **Namespace:** Microsoft::WRL::Details  
  
## See Also  
 [Microsoft::WRL::Details Namespace](../vs140/Microsoft--WRL--Details-Namespace.md)