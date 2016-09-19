---
title: "PROP_ENTRY_INTERFACE_CALLBACK_EX"
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
ms.assetid: af9f61a1-6a69-4d9f-bebd-8e638a6ab99d
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# PROP_ENTRY_INTERFACE_CALLBACK_EX
Lets you specify a particular IID if your object supports multiple dispatch interfaces. Resembles [PROP_ENTRY_INTERFACE_CALLBACK](../vs140/PROP_ENTRY_INTERFACE_CALLBACK.md).  
  
## Syntax  
  
```  
PROP_ENTRY_INTERFACE_CALLBACK_EX(  
   szDesc,  
   dispid,  
   clsid,  
   iidDispatch,  
   pfnFunc,  
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
  
 [in] `iidDispatch`  
 The IID of the dispatch interface that defines the property.  
  
 [in]`pfnFunc`  
 The callback function that controls data during the loading process.  
  
 [in] `vt`  
 The type of the property.  
  
## Remarks  
 Include this macro to give an application more control over the [IPersistStreamInitImpl::Load](../vs140/IPersistStreamInitImpl--Load.md) process. The callback function `pfnFunc` is called when `IPersistStreamInitImpl::Load` is retrieving data from a non-trusted stream. The callback function filters the data and controls which objects are loaded.  
  
 This macro only applies if `IPersistStreamInitImpl` is a base class and the class is advertised as safe for initialization. Otherwise, you should not use this macro.  
  
 This macro is only valid if `vt` is `VT_DISPATCH` or `VT_UNKNOWN`. Passing in a different value for `vt` to this macro will cause a compilation error. For any other value of `vt`, use [PROP_ENTRY_TYPE_EX](../vs140/PROP_ENTRY_TYPE_EX.md).  
  
 The [BEGIN_PROP_MAP](../vs140/BEGIN_PROP_MAP.md) macro marks the beginning of the property map; the [END_PROP_MAP](../vs140/END_PROP_MAP.md) macro marks the end.  
  
 If you are creating a web control that needs to be initialized, you should use the [IPersistPropertyBagImpl Class](../vs140/IPersistPropertyBagImpl-Class.md) instead of `IPersistStreamInitImpl` to initialize properties. `IPersistStreamInitImpl` possess a greater risk in binary format than `IPersistPropertyBagImpl`.  
  
## Example  
 See the example for [BEGIN_PROP_MAP](../vs140/BEGIN_PROP_MAP.md).  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [ATL Macros Alphabetical Reference](../vs140/ATL-Macros-Alphabetical-Reference.md)   
 [PROP_ENTRY_INTERFACE](../vs140/PROP_ENTRY_INTERFACE.md)   
 [PROP_ENTRY_INTERFACE_EX](../vs140/PROP_ENTRY_INTERFACE_EX.md)   
 [PROP_ENTRY_INTERFACE_CALLBACK](../vs140/PROP_ENTRY_INTERFACE_CALLBACK.md)   
 [PROP_ENTRY_TYPE](../vs140/PROP_ENTRY_TYPE.md)   
 [PROP_ENTRY_TYPE_EX](../vs140/PROP_ENTRY_TYPE_EX.md)