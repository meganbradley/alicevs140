---
title: "Label (Debug Interface Access SDK)"
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
ms.assetid: 8cef7620-5bc8-4500-8bd0-e9e638bccb24
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Label (Debug Interface Access SDK)
A location in program code is identified by a `SymTagLabel` symbol.  
  
## Properties  
 The following table shows the properties that are valid for this symbol type.  
  
|Property|Data type|Description|  
|--------------|---------------|-----------------|  
|[IDiaSymbol::get_addressOffset](../vs140/IDiaSymbol--get_addressOffset.md)|`DWORD`|Offset part of location; for details, see the [LocationType Enumeration](../vs140/LocationType.md).|  
|[IDiaSymbol::get_addressSection](../vs140/IDiaSymbol--get_addressSection.md)|`DWORD`|Section part of location; for details, see the [LocationType Enumeration](../vs140/LocationType.md).|  
|[customCallingConvention](../vs140/IDiaSymbol--get_customCallingConvention.md)|`BOOL`|`TRUE` if the label uses a custom calling convention.|  
|[farReturn](../vs140/IDiaSymbol--get_farReturn.md)|`BOOL`|`TRUE` if label performs a far return.|  
|[interruptReturn](../vs140/IDiaSymbol--get_interruptReturn.md)|`BOOL`|`TRUE` if label contains a return from interrupt.|  
|[IDiaSymbol::get_lexicalParent](../vs140/IDiaSymbol--get_lexicalParent.md)|`IDiaSymbol*`|Symbol for the enclosing compiland, block, or function.|  
|[lexicalParentId](../vs140/IDiaSymbol--get_lexicalParentId.md)|`DWORD`|ID of the lexical parent symbol.|  
|[IDiaSymbol::get_locationType](../vs140/IDiaSymbol--get_locationType.md)|`DWORD`|Labels have static locations; for details, see the [Symbol Locations](../vs140/Symbol-Locations.md) enumeration.|  
|[name](../vs140/IDiaSymbol--get_name.md)|`BSTR`|The label's name.|  
|[noInline](../vs140/IDiaSymbol--get_noInline.md)|`BOOL`|`TRUE` if the label was specified with the [noinline](../vs140/noinline.md) attribute.|  
|[noReturn](../vs140/IDiaSymbol--get_noReturn.md)|`BOOL`|`TRUE` if the label was specified with the [noreturn](../vs140/noreturn.md) attribute.|  
|[notReached](../vs140/IDiaSymbol--get_notReached.md)|`BOOL`|`TRUE` if the label is never called.|  
|[offset](../vs140/IDiaSymbol--get_offset.md)|`LONG`|Offset of symbol in memory; for details, see the [LocationType Enumeration](../vs140/LocationType.md), `LocIsRegRel`.|  
|[optimizedCodeDebugInfo](../vs140/IDiaSymbol--get_optimizedCodeDebugInfo.md)|`BOOL`|`TRUE` if the code has debug information for optimized code.|  
|[relativeVirtualAddress](../vs140/IDiaSymbol--get_relativeVirtualAddress.md)|`DWORD`|Relative position of this label within its module.|  
|[IDiaSymbol::get_symIndexId Method](../vs140/IDiaSymbol--get_symIndexId.md)|`DWORD`|Index ID of symbol.|  
|[symTag](../vs140/IDiaSymbol--get_symTag.md)|`DWORD`|Returns `SymTagFuncDebugLabel` (one of the [SymTagEnum Enumeration](../vs140/SymTagEnum.md) values).|  
|[virtualAddress](../vs140/IDiaSymbol--get_virtualAddress.md)|`ULONGLONG`|Position of this label within the executable image.|  
  
## See Also  
 [Lexical Hierarchy of Symbol Types](../vs140/Lexical-Hierarchy-of-Symbol-Types.md)   
 [LocationType Enumeration](../vs140/LocationType.md)   
 [Symbol Locations](../vs140/Symbol-Locations.md)