---
title: "COM_INTERFACE_ENTRY_AGGREGATE"
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
ms.assetid: c671fa40-a57b-4797-ae88-c9762dabd4dc
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COM_INTERFACE_ENTRY_AGGREGATE
When the interface identified by `iid` is queried for, `COM_INTERFACE_ENTRY_AGGREGATE` forwards to `punk`.  
  
## Syntax  
  
```  
  
COM_INTERFACE_ENTRY_AGGREGATE(   
iid  
,   
punk  
 )  
  
```  
  
#### Parameters  
 `iid`  
 [in] The GUID of the interface queried for.  
  
 `punk`  
 [in] The name of an **IUnknown** pointer.  
  
## Remarks  
 The `punk` parameter is assumed to point to the inner unknown of an aggregate or to **NULL**, in which case the entry is ignored. Typically, you would **CoCreate** the aggregate in `FinalConstruct`.  
  
 See [COM_INTERFACE_ENTRY Macros](../vs140/COM_INTERFACE_ENTRY-Macros.md) for remarks about COM map entries.  
  
## Example  
 [!CODE [NVC_ATL_Windowing#112](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#112)]  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [COM Map Macros](../vs140/COM-Map-Macros.md)   
 [Macros](../vs140/ATL-Macros.md)