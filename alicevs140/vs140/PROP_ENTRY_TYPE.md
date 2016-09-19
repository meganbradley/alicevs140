---
title: "PROP_ENTRY_TYPE"
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
ms.assetid: 172466f3-a512-41dd-9289-841f29ab150d
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# PROP_ENTRY_TYPE
Use this macro to enter a property description, property DISPID, and property page CLSID into the object's property map.  
  
## Syntax  
  
```  
PROP_ENTRY_TYPE(   
   szDesc,   
   dispid,   
   clsid,   
   vt   
)  
```  
  
#### Parameters  
 `szDesc`  
 [in] The property description.  
  
 `dispid`  
 [in] The property's DISPID.  
  
 `clsid`  
 [in] The CLSID of the associated property page. Use the special value `CLSID_NULL` for a property that does not have an associated property page.  
  
 `vt`  
 [in] The property's type.  
  
## Remarks  
 The `PROP_ENTRY` macro was insecure and deprecated. It has been replaced with `PROP_ENTRY_TYPE`.  
  
 The [BEGIN_PROP_MAP](../vs140/BEGIN_PROP_MAP.md) macro marks the beginning of the property map; the [END_PROP_MAP](../vs140/END_PROP_MAP.md) macro marks the end.  
  
## Example  
 See the example for [BEGIN_PROP_MAP](../vs140/BEGIN_PROP_MAP.md).  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [Property Map Macros](../vs140/Property-Map-Macros.md)   
 [Macros](../vs140/ATL-Macros.md)   
 [PROP_ENTRY_TYPE_EX](../vs140/PROP_ENTRY_TYPE_EX.md)   
 [PROP_PAGE](../vs140/PROP_PAGE.md)   
 [PROP_ENTRY_INTERFACE](../vs140/PROP_ENTRY_INTERFACE.md)   
 [PROP_ENTRY_INTERFACE_EX](../vs140/PROP_ENTRY_INTERFACE_EX.md)   
 [PROP_ENTRY_INTERFACE_CALLBACK](../vs140/PROP_ENTRY_INTERFACE_CALLBACK.md)   
 [PROP_ENTRY_INTERFACE_CALLBACK_EX](../vs140/PROP_ENTRY_INTERFACE_CALLBACK_EX.md)