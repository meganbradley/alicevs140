---
title: "Module::UnregisterWinRTObject Method"
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
ms.assetid: 32334aa7-2293-40d2-9a89-4b02e2e31f3c
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Module::UnregisterWinRTObject Method
Unregisters one or more [!INCLUDE[wrt](../vs140/includes/wrt_md.md)] objects so that other applications cannot connect to them.  
  
## Syntax  
  
```  
virtual HRESULT UnregisterWinRTObject(  
   unsigned int,  
   _Inout_ WINRT_REGISTRATION_COOKIE* cookie  
);  
  
```  
  
#### Parameters  
 `cookie`  
 A pointer to a value that identifies the class object whose registration is to be revoked.  
  
## Return Value  
  
## Requirements  
 **Header:** module.h  
  
 **Namespace:** Microsoft::WRL  
  
## See Also  
 [Module Class](../vs140/Module-Class.md)