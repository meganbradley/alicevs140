---
title: "PROP_ENTRY_INTERFACE"
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
ms.assetid: b556ff4f-2705-488c-989d-d98fda80036c
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# PROP_ENTRY_INTERFACE
Lets you enter a property description, a property DISPID, and a list of property page CLSIDs into the property map for the object.  
  
## Syntax  
  
```  
PROP_ENTRY_INTERFACE(  
   szDesc,  
   dispid,  
   clsid,  
   rgclsidAllowed,  
   cclsidAllowed,  
   vt  
)  
```  
  
#### Parameters  
 [in] `szDesc`  
 The property description.  
  
 [in] `dispid`  
 The DISPID of the property.  
  
 [in] `clsid`  
 The CLSID of the associated property page. Use the special value `CLSID_NULL` for a property that does not have an associated property page.  
  
 [in] `rgclsidAllowed`  
 An array of CLSIDs that can be loaded. For stability, use a `const` array.  
  
 [in] `cclsidAllowed`  
 The number of elements in `rgclsidAllowed`.  
  
 [in] `vt`  
 The type for the property.  
  
## Remarks  
 Include this macro to give an application more control over the [IPersistStreamInitImpl::Load](../vs140/IPersistStreamInitImpl--Load.md) process. This macro only applies if `IPersistStreamInitImpl` is a base class and the class is advertised as safe for initializing. Otherwise, you should not use this macro.  
  
 In most cases, `cclsidAllowed` can be determined by `_countof(rgclsidAllowed)`.  
  
 This macro is only valid if `vt` is `VT_DISPATCH` or `VT_UNKNOWN`. Passing in a different value for `vt` to this macro will result in a compilation error. For any other value of `vt`, use [PROP_ENTRY_TYPE](../vs140/PROP_ENTRY_TYPE.md).  
  
 The [BEGIN_PROP_MAP](../vs140/BEGIN_PROP_MAP.md) macro marks the beginning of the property map; the [END_PROP_MAP](../vs140/END_PROP_MAP.md) macro marks the end.  
  
 If you are creating a web control that needs to be initialized, you should use the [IPersistPropertyBagImpl Class](../vs140/IPersistPropertyBagImpl-Class.md) instead of `IPersistStreamInitImpl` to initialize properties. `IPersistStreamInitImpl` possess a greater risk in binary format than `IPersistPropertyBagImpl`.  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [ATL Macros Alphabetical Reference](../vs140/ATL-Macros-Alphabetical-Reference.md)   
 [PROP_ENTRY_INTERFACE_EX](../vs140/PROP_ENTRY_INTERFACE_EX.md)   
 [PROP_ENTRY_INTERFACE_CALLBACK](../vs140/PROP_ENTRY_INTERFACE_CALLBACK.md)   
 [PROP_ENTRY_INTERFACE_CALLBACK_EX](../vs140/PROP_ENTRY_INTERFACE_CALLBACK_EX.md)   
 [PROP_ENTRY_TYPE](../vs140/PROP_ENTRY_TYPE.md)   
 [PROP_ENTRY_TYPE_EX](../vs140/PROP_ENTRY_TYPE_EX.md)