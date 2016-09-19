---
title: "DECLARE_PROTECT_FINAL_CONSTRUCT"
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
ms.assetid: 2d2e5ddc-057a-43ca-87c8-d3477a8193a0
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DECLARE_PROTECT_FINAL_CONSTRUCT
Protects your object from being deleted if (during [FinalConstruct](../vs140/CComObjectRootEx--FinalConstruct.md)) the internal aggregated object increments the reference count then decrements the count to 0.  
  
## Syntax  
  
```  
  
DECLARE_PROTECT_FINAL_CONSTRUCT( )  
  
```  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [Aggregation and Class Factory Macros](../vs140/Aggregation-and-Class-Factory-Macros.md)   
 [Macros](../vs140/ATL-Macros.md)