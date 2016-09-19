---
title: "SERVICE_ENTRY_CHAIN"
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
ms.assetid: 09be4ce4-3ccd-4ff2-a95e-a9d5275354c1
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# SERVICE_ENTRY_CHAIN
Instructs [IServiceProviderImpl::QueryService](../vs140/IServiceProviderImpl--QueryService.md) to chain to the object specified by `punk`.  
  
## Syntax  
  
```  
  
      SERVICE_ENTRY_CHAIN(   
   punk    
)  
```  
  
#### Parameters  
 `punk`  
 A pointer to the **IUnknown** interface to which to chain.  
  
## Example  
 See the example for [BEGIN_SERVICE_MAP](../vs140/BEGIN_SERVICE_MAP.md).  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [Service Map Macros](../vs140/Service-Map-Macros.md)   
 [Macros](../vs140/ATL-Macros.md)   
 [SERVICE_ENTRY](../vs140/SERVICE_ENTRY.md)   
 [BEGIN_SERVICE_MAP](../vs140/BEGIN_SERVICE_MAP.md)   
 [END_SERVICE_MAP](../vs140/END_SERVICE_MAP.md)