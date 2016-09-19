---
title: "BEGIN_COM_MAP"
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
ms.assetid: ead2a1e3-334d-44ad-bb1f-b94bb14c2333
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# BEGIN_COM_MAP
The COM map is the mechanism that exposes interfaces on an object to a client through `QueryInterface`.  
  
## Syntax  
  
```  
  
BEGIN_COM_MAP( x )  
```  
  
#### Parameters  
 *x*  
 [in] The name of the class object you are exposing interfaces on.  
  
## Remarks  
 [CComObjectRootEx::InternalQueryInterface](../vs140/CComObjectRootEx--InternalQueryInterface.md) only returns pointers for interfaces in the COM map. Start your interface map with the `BEGIN_COM_MAP` macro, add entries for each of your interfaces with the [COM_INTERFACE_ENTRY](../vs140/COM_INTERFACE_ENTRY--ATL-.md) macro or one of its variants, and complete the map with the [END_COM_MAP](../vs140/END_COM_MAP.md) macro.  
  
## Example  
 From the ATL [BEEPER](../vs140/Visual-C---Samples.md) sample:  
  
 [!CODE [NVC_ATL_COM#1](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_COM#1)]  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [COM Map Macros](../vs140/COM-Map-Macros.md)   
 [Macros](../vs140/ATL-Macros.md)