---
title: "COM_INTERFACE_ENTRY_CHAIN"
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
ms.assetid: 0eb40174-d703-4ce4-a424-d65c3aa7e7c5
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COM_INTERFACE_ENTRY_CHAIN
Processes the COM map of the base class when the processing reaches this entry in the COM map.  
  
## Syntax  
  
```  
  
COM_INTERFACE_ENTRY_CHAIN(   
classname  
 )  
  
```  
  
#### Parameters  
 *classname*  
 [in] A base class of the current object.  
  
## Remarks  
 For example, in the following code:  
  
 [!CODE [NVC_ATL_Windowing#116](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#116)]  
  
 Note that the first entry in the COM map must be an interface on the object containing the COM map. Thus, you cannot start your COM map entries with `COM_INTERFACE_ENTRY_CHAIN`, which causes the COM map of a different object to be searched at the point where **COM_INTERFACE_ENTRY_CHAIN(**`COtherObject`**)** appears in your object's COM map. If you want to search the COM map of another object first, add an interface entry for **IUnknown** to your COM map, then chain the other object's COM map. For example:  
  
 [!CODE [NVC_ATL_Windowing#111](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#111)]  
  
 See [COM_INTERFACE_ENTRY Macros](../vs140/COM_INTERFACE_ENTRY-Macros.md) for remarks about COM map entries.  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [COM Map Macros](../vs140/COM-Map-Macros.md)   
 [Macros](../vs140/ATL-Macros.md)