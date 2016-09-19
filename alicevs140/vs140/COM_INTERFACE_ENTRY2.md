---
title: "COM_INTERFACE_ENTRY2"
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
ms.assetid: 3d48c53b-827b-42cc-9e22-594f7ea2bf0b
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COM_INTERFACE_ENTRY2
Use this macro to disambiguate two branches of inheritance.  
  
## Syntax  
  
```  
  
COM_INTERFACE_ENTRY2(   
x  
,   
x2  
 )  
  
```  
  
#### Parameters  
 *x*  
 [in] The name of an interface you want to expose from your object.  
  
 `x2`  
 [in] The name of the inheritance branch from which *x* is exposed.  
  
## Remarks  
 For example, if you derive your class object from two dual interfaces, you expose `IDispatch` using `COM_INTERFACE_ENTRY2` since `IDispatch` can be obtained from either one of the interfaces.  
  
 See [COM_INTERFACE_ENTRY Macros](../vs140/COM_INTERFACE_ENTRY-Macros.md) for remarks about COM map entries.  
  
## Example  
 [!CODE [NVC_ATL_Windowing#118](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#118)]  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [COM Map Macros](../vs140/COM-Map-Macros.md)   
 [Macros](../vs140/ATL-Macros.md)