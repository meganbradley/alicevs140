---
title: "UdtKind"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 400b59b9-373c-42cb-aae1-570494214328
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# UdtKind
Describes the variety of user-defined type (UDT).  
  
## Syntax  
  
```cpp#  
enum UdtKind {   
   UdtStruct,  
   UdtClass,  
   UdtUnion,  
   UdtInterface  
};  
```  
  
## Elements  
 UdtStruct  
 UDT is a structure.  
  
 UdtClass  
 UDT is a class.  
  
 UdtUnion  
 UDT is a union.  
  
 UdtInterface  
 UDT is an interface.  
  
## Remarks  
 The values in this enumeration are returned by the [IDiaSymbol::get_udtKind](../vs140/IDiaSymbol--get_udtKind.md) method.  
  
## Requirements  
 Header: cvconst.h  
  
## See Also  
 [Enumerations and Structures](../vs140/Enumerations-and-Structures.md)   
 [IDiaSymbol::get_udtKind](../vs140/IDiaSymbol--get_udtKind.md)