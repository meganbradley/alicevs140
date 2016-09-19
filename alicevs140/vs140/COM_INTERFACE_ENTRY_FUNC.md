---
title: "COM_INTERFACE_ENTRY_FUNC"
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
ms.assetid: e4c9936b-0957-4172-a3ca-b715d6909966
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COM_INTERFACE_ENTRY_FUNC
A general mechanism for hooking into ATL's `QueryInterface` logic.  
  
## Syntax  
  
```  
  
COM_INTERFACE_ENTRY_FUNC(   
iid  
,   
dw  
,   
func  
 )  
  
```  
  
#### Parameters  
 `iid`  
 [in] The GUID of the interface exposed.  
  
 `dw`  
 [in] A parameter passed through to the `func`.  
  
 `func`  
 [in] The function pointer that will return `iid`.  
  
## Remarks  
 If *iid* matches the IID of the interface queried for, then the function specified by `func` is called. The declaration for the function should be:  
  
 `HRESULT WINAPI func(void* pv, REFIID riid, LPVOID* ppv, DWORD_PTR dw);`  
  
 When your function is called, `pv` points to your class object. The `riid` parameter refers to the interface being queried for, `ppv` is the pointer to the location where the function should store the pointer to the interface, and `dw` is the parameter you specified in the entry. The function should set \*`ppv` to **NULL** and return **E_NOINTERFACE** or **S_FALSE** if it chooses not to return an interface. With **E_NOINTERFACE**, COM map processing terminates. With **S_FALSE**, COM map processing continues, even though no interface pointer was returned. If the function returns an interface pointer, it should return `S_OK`.  
  
 See [COM_INTERFACE_ENTRY Macros](../vs140/COM_INTERFACE_ENTRY-Macros.md) for remarks about COM map entries.  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [COM Map Macros](../vs140/COM-Map-Macros.md)   
 [Macros](../vs140/ATL-Macros.md)