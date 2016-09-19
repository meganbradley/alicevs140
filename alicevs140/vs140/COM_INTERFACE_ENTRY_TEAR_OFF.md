---
title: "COM_INTERFACE_ENTRY_TEAR_OFF"
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
ms.assetid: 3ccaa1ec-a608-473f-83cd-525a1b2e0274
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COM_INTERFACE_ENTRY_TEAR_OFF
Exposes your tear-off interfaces.  
  
## Syntax  
  
```  
  
COM_INTERFACE_ENTRY_TEAR_OFF(   
iid  
,   
x  
 )  
  
```  
  
#### Parameters  
 `iid`  
 [in] The GUID of the tear-off interface.  
  
 *x*  
 [in] The name of the class implementing the interface.  
  
## Remarks  
 A tear-off interface is implemented as a separate object that is instantiated every time the interface it represents is queried for. Typically, you build your interface as a tear-off if the interface is rarely used, since this saves a vtable pointer in every instance of your main object. The tear-off is deleted when its reference count becomes zero. The class implementing the tear-off should be derived from `CComTearOffObjectBase` and have its own COM map.  
  
 See [COM_INTERFACE_ENTRY Macros](../vs140/COM_INTERFACE_ENTRY-Macros.md) for remarks about COM map entries.  
  
## Example  
 [!CODE [NVC_ATL_COM#1](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_COM#1)]  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [COM Map Macros](../vs140/COM-Map-Macros.md)   
 [Macros](../vs140/ATL-Macros.md)