---
title: "PROP_ENTRY_TYPE_EX"
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
ms.assetid: 61df460c-854e-4d42-87dc-5fc3894b58aa
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# PROP_ENTRY_TYPE_EX
Similar to [PROP_ENTRY_TYPE](../vs140/PROP_ENTRY_TYPE.md), but allows you specify a particular IID if your object supports multiple dual interfaces.  
  
## Syntax  
  
```  
PROP_ENTRY_TYPE_EX(   
   szDesc,   
   dispid,   
   clsid,   
   iidDispatch,   
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
  
 `iidDispatch`  
 [in] The IID of the dual interface defining the property.  
  
 `vt`  
 [in] The property's type.  
  
## Remarks  
 The `PROP_ENTRY_EX` macro was insecure and deprecated. It has been replaced with `PROP_ENTRY_TYPE_EX`.  
  
 The [BEGIN_PROP_MAP](../vs140/BEGIN_PROP_MAP.md) macro marks the beginning of the property map; the [END_PROP_MAP](../vs140/END_PROP_MAP.md) macro marks the end.  
  
## Example  
 The following example groups entries for `IMyDual1` followed by an entry for `IMyDual2`. Grouping by dual interface will improve performance.  
  
 [!CODE [NVC_ATL_Windowing#133](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#133)]  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [Property Map Macros](../vs140/Property-Map-Macros.md)   
 [Macros](../vs140/ATL-Macros.md)   
 [PROP_PAGE](../vs140/PROP_PAGE.md)   
 [PROP_ENTRY_INTERFACE](../vs140/PROP_ENTRY_INTERFACE.md)   
 [PROP_ENTRY_INTERFACE_EX](../vs140/PROP_ENTRY_INTERFACE_EX.md)   
 [PROP_ENTRY_INTERFACE_CALLBACK](../vs140/PROP_ENTRY_INTERFACE_CALLBACK.md)   
 [PROP_ENTRY_INTERFACE_CALLBACK_EX](../vs140/PROP_ENTRY_INTERFACE_CALLBACK_EX.md)   
 [PROP_ENTRY_TYPE](../vs140/PROP_ENTRY_TYPE.md)