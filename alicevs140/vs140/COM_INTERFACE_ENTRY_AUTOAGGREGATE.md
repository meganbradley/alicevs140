---
title: "COM_INTERFACE_ENTRY_AUTOAGGREGATE"
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
ms.assetid: c191a812-31ae-4667-bf67-109ba158e933
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COM_INTERFACE_ENTRY_AUTOAGGREGATE
Same as [COM_INTERFACE_ENTRY_AGGREGATE](../vs140/COM_INTERFACE_ENTRY_AGGREGATE.md), except if `punk` is **NULL**, it automatically creates the aggregate described by the `clsid`.  
  
## Syntax  
  
```  
  
COM_INTERFACE_ENTRY_AUTOAGGREGATE(   
iid  
,   
punk  
,   
clsid  
 )  
  
```  
  
#### Parameters  
 `iid`  
 [in] The GUID of the interface queried for.  
  
 `punk`  
 [in] The name of an **IUnknown** pointer. Must be a member of the class containing the COM map.  
  
 `clsid`  
 [in] The identifier of the aggregate that will be created if `punk` is **NULL**.  
  
## Remarks  
 See [COM_INTERFACE_ENTRY Macros](../vs140/COM_INTERFACE_ENTRY-Macros.md) for remarks about COM map entries.  
  
## Example  
 [!CODE [NVC_ATL_Windowing#114](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#114)]  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [COM Map Macros](../vs140/COM-Map-Macros.md)   
 [Macros](../vs140/ATL-Macros.md)