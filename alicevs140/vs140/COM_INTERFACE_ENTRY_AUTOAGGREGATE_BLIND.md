---
title: "COM_INTERFACE_ENTRY_AUTOAGGREGATE_BLIND"
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
ms.assetid: 4e867f24-0a4f-465e-ad17-06939fcf9c1c
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COM_INTERFACE_ENTRY_AUTOAGGREGATE_BLIND
Same as [COM_INTERFACE_ENTRY_AUTOAGGREGATE](../vs140/COM_INTERFACE_ENTRY_AUTOAGGREGATE.md), except that querying for any IID results in forwarding the query to `punk`, and if `punk` is **NULL**, automatically creating the aggregate described by the `clsid`.  
  
## Syntax  
  
```  
  
COM_INTERFACE_ENTRY_AUTOAGGREGATE_BLIND(   
punk  
,   
clsid  
 )  
  
```  
  
#### Parameters  
 `punk`  
 [in] The name of an **IUnknown** pointer. Must be a member of the class containing the COM map.  
  
 `clsid`  
 [in] The identifier of the aggregate that will be created if `punk` is **NULL**.  
  
## Remarks  
 If the interface query fails, processing of the COM map continues.  
  
 See [COM_INTERFACE_ENTRY Macros](../vs140/COM_INTERFACE_ENTRY-Macros.md) for remarks about COM map entries.  
  
## Example  
 [!CODE [NVC_ATL_Windowing#115](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#115)]  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [COM Map Macros](../vs140/COM-Map-Macros.md)   
 [Macros](../vs140/ATL-Macros.md)