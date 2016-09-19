---
title: "BEGIN_SERVICE_MAP"
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
ms.assetid: 3c6ae156-8776-4588-8227-2d234daec236
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# BEGIN_SERVICE_MAP
Marks the beginning of the service map.  
  
## Syntax  
  
```  
  
BEGIN_SERVICE_MAP( theClass )  
```  
  
#### Parameters  
 `theClass`  
 [in] Specifies the class containing the service map.  
  
## Remarks  
 Use the service map to implement service provider functionality on your COM object. First, you must derive your class from [IServiceProviderImpl](../vs140/IServiceProviderImpl-Class.md). There are two types of entries:  
  
-   [SERVICE_ENTRY](../vs140/SERVICE_ENTRY.md) Indicates support for the specified service ID (SID).  
  
-   [SERVICE_ENTRY_CHAIN](../vs140/SERVICE_ENTRY_CHAIN.md) Instructs [IServiceProviderImpl::QueryService](../vs140/IServiceProviderImpl--QueryService.md) to chain to another, specified object.  
  
## Example  
 [!CODE [NVC_ATL_COM#57](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_COM#57)]  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [Service Map Macros](../vs140/Service-Map-Macros.md)   
 [Macros](../vs140/ATL-Macros.md)   
 [END_SERVICE_MAP](../vs140/END_SERVICE_MAP.md)