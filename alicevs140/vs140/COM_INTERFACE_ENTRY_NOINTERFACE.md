---
title: "COM_INTERFACE_ENTRY_NOINTERFACE"
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
ms.assetid: 14a9e65f-bb02-4d48-9eba-c32b8a71b0e0
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COM_INTERFACE_ENTRY_NOINTERFACE
Returns **E_NOINTERFACE** and terminates COM map processing when the specified interface is queried for.  
  
## Syntax  
  
```  
  
COM_INTERFACE_ENTRY_NOINTERFACE(   
x  
 )  
  
```  
  
#### Parameters  
 *x*  
 [in] Text used to construct the interface identifier.  
  
## Remarks  
 You can use this macro to prevent an interface from being used in a particular case. For example, you can insert this macro into your COM map right before `COM_INTERFACE_ENTRY_AGGREGATE_BLIND` to prevent a query for the interface from being forwarded to the aggregate's inner unknown.  
  
 The interface IID will be constructed by appending *x* to `IID_`. For example, if *x* is `IPersistStorage`, the IID will be `IID_IPersistStorage`.  
  
 See [COM_INTERFACE_ENTRY Macros](../vs140/COM_INTERFACE_ENTRY-Macros.md) for remarks about COM map entries.  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [COM Map Macros](../vs140/COM-Map-Macros.md)   
 [Macros](../vs140/ATL-Macros.md)