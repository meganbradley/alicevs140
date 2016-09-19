---
title: "FuncDebugEnd"
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
ms.assetid: 68f84fff-7cd3-4636-b929-7063a45009f8
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# FuncDebugEnd
If a function has a defined point at which debugging is to end, the debug starting point is identified by a symbol with a `SymTagFuncDebugEnd` tag.  
  
## Properties  
 The following table shows the properties that are valid for this symbol type.  
  
|Property|Data type|Description|  
|--------------|---------------|-----------------|  
|[IDiaSymbol::get_addressOffset](../vs140/IDiaSymbol--get_addressOffset.md)|`DWORD`|Offset part of location; for details, see the [LocationType Enumeration](../vs140/LocationType.md).|  
|[IDiaSymbol::get_addressSection](../vs140/IDiaSymbol--get_addressSection.md)|`DWORD`|Section part of location; for details, see the [LocationType Enumeration](../vs140/LocationType.md).|  
|[customCallingConvention](../vs140/IDiaSymbol--get_customCallingConvention.md)|`BOOL`|`TRUE` if the function uses a custom calling convention (only in DIA SDK V8.0 or later).|  
|[farReturn](../vs140/IDiaSymbol--get_farReturn.md)|`BOOL`|`TRUE` if function performs a far return (only in DIA SDK V8.0 or later).|  
|[interruptReturn](../vs140/IDiaSymbol--get_interruptReturn.md)|`BOOL`|`TRUE` if function contains a return from interrupt (only in DIA SDK V8.0 or later).|  
|[isStatic](../vs140/IDiaSymbol--get_isStatic.md)|`BOOL`|`TRUE` if the function is static (only in DIA SDK V8.0 or later).|  
|[IDiaSymbol::get_lexicalParent](../vs140/IDiaSymbol--get_lexicalParent.md)|`IDiaSymbol*`|Symbol for the enclosing function.|  
|[lexicalParentId](../vs140/IDiaSymbol--get_lexicalParentId.md)|`DWORD`|ID of the lexical parent symbol.|  
|[IDiaSymbol::get_locationType](../vs140/IDiaSymbol--get_locationType.md)|`DWORD`|End points have static location; for details, see [Symbol Locations](../vs140/Symbol-Locations.md).|  
|[noInline](../vs140/IDiaSymbol--get_noInline.md)|`BOOL`|`TRUE` if the function was specified with the [noinline](../vs140/noinline.md) attribute (only in DIA SDK V8.0 or later).|  
|[noReturn](../vs140/IDiaSymbol--get_noReturn.md)|`BOOL`|`TRUE` if the function was specified with the [noreturn](../vs140/noreturn.md) attribute (only in DIA SDK V8.0 or later).|  
|[notReached](../vs140/IDiaSymbol--get_notReached.md)|`BOOL`|`TRUE` if the function is never called (only in DIA SDK V8.0 or later).|  
|[offset](../vs140/IDiaSymbol--get_offset.md)|`LONG`|Offset of symbol in memory; for details, see the [LocationType Enumeration](../vs140/LocationType.md), `LocIsRegRel`.|  
|[optimizedCodeDebugInfo](../vs140/IDiaSymbol--get_optimizedCodeDebugInfo.md)|`BOOL`|`TRUE` if the function has debug information for optimized code (only in DIA SDK V8.0 or later).|  
|[IDiaSymbol::get_symIndexId Method](../vs140/IDiaSymbol--get_symIndexId.md)|`DWORD`|Index ID of symbol.|  
|[relativeVirtualAddress](../vs140/IDiaSymbol--get_relativeVirtualAddress.md)|`DWORD`|Relative position of the end of this function within its module.|  
|[symTag](../vs140/IDiaSymbol--get_symTag.md)|`DWORD`|Returns `SymTagFuncDebugEnd` (one of the [SymTagEnum Enumeration](../vs140/SymTagEnum.md) values).|  
|[virtualAddress](../vs140/IDiaSymbol--get_virtualAddress.md)|`ULONGLONG`|Position of this function within the executable image.|  
  
## See Also  
 [Lexical Hierarchy of Symbol Types](../vs140/Lexical-Hierarchy-of-Symbol-Types.md)   
 [LocationType Enumeration](../vs140/LocationType.md)   
 [Symbol Locations](../vs140/Symbol-Locations.md)