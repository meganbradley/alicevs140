---
title: "Annotation"
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
ms.assetid: eb9f759b-98a5-45fc-b085-91f1f2666e72
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Annotation
A location program code can be annotated with a `SymTagAnnotation` symbol.  
  
## Properties  
 The following table shows the properties that are valid for this symbol type.  
  
|Property|Data type|Description|  
|--------------|---------------|-----------------|  
|[IDiaSymbol::get_addressOffset](../vs140/IDiaSymbol--get_addressOffset.md)|`DWORD`|Offset part of location; for details, see the [LocationType Enumeration](../vs140/LocationType.md).|  
|[IDiaSymbol::get_addressSection](../vs140/IDiaSymbol--get_addressSection.md)|`DWORD`|Section part of location; for details, see the [LocationType Enumeration](../vs140/LocationType.md).|  
|[IDiaSymbol::get_dataKind](../vs140/IDiaSymbol--get_dataKind.md)|`DWORD`|One of the [DataKind Enumeration](../vs140/DataKind.md) values.|  
|[relativeVirtualAddress](../vs140/IDiaSymbol--get_relativeVirtualAddress.md)|`DWORD`|Relative position of this annotation within its module.|  
|[IDiaSymbol::get_symIndexId Method](../vs140/IDiaSymbol--get_symIndexId.md)|`DWORD`|Index ID of symbol.|  
|[symTag](../vs140/IDiaSymbol--get_symTag.md)|`DWORD`|Returns `SymTagAnnotation` (one of the [SymTagEnum Enumeration](../vs140/SymTagEnum.md) values).|  
|[IDiaSymbol::get_value](../vs140/IDiaSymbol--get_value.md)|`VARIANT`|The value of constant data.|  
|[virtualAddress](../vs140/IDiaSymbol--get_virtualAddress.md)|`ULONGLONG`|Position of this annotation within the executable image.|  
  
## See Also  
 [Lexical Hierarchy of Symbol Types](../vs140/Lexical-Hierarchy-of-Symbol-Types.md)   
 [LocationType Enumeration](../vs140/LocationType.md)   
 [Symbol Locations](../vs140/Symbol-Locations.md)