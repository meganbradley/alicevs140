---
title: "COM_INTERFACE_ENTRY_AGGREGATE_BLIND"
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
ms.assetid: c44e4d89-0f33-4eca-9ded-18a35311f94f
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COM_INTERFACE_ENTRY_AGGREGATE_BLIND
Same as [COM_INTERFACE_ENTRY_AGGREGATE](../vs140/COM_INTERFACE_ENTRY_AGGREGATE.md), except that querying for any IID results in forwarding the query to `punk`.  
  
## Syntax  
  
```  
  
COM_INTERFACE_ENTRY_AGGREGATE_BLIND(   
punk  
 )  
  
```  
  
#### Parameters  
 `punk`  
 [in] The name of an **IUnknown** pointer.  
  
## Remarks  
 If the interface query fails, processing of the COM map continues.  
  
 See [COM_INTERFACE_ENTRY Macros](../vs140/COM_INTERFACE_ENTRY-Macros.md) for remarks about COM map entries.  
  
## Example  
 [!CODE [NVC_ATL_Windowing#113](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#113)]  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [COM Map Macros](../vs140/COM-Map-Macros.md)   
 [Macros](../vs140/ATL-Macros.md)