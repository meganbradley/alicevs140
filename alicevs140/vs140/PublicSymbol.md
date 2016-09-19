---
title: "PublicSymbol"
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
ms.assetid: f8d33007-302d-4549-9dad-47fb33ea60b7
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# PublicSymbol
When the .exe file is created, each public symbol (at a minimum, each global function and data symbol) is given a `SymTagPublicSymbol` tag.  
  
## Properties  
 The following table shows the properties that are valid for this symbol type.  
  
|Property|Data type|Description|  
|--------------|---------------|-----------------|  
|[IDiaSymbol::get_addressOffset](../vs140/IDiaSymbol--get_addressOffset.md)|`DWORD`|Offset part of location; for details, see the [LocationType Enumeration](../vs140/LocationType.md).|  
|[IDiaSymbol::get_addressSection](../vs140/IDiaSymbol--get_addressSection.md)|`DWORD`|Section part of location; for details, see the [LocationType Enumeration](../vs140/LocationType.md).|  
|[IDiaSymbol::get_code](../vs140/IDiaSymbol--get_code.md)|`BOOL`|`TRUE` if the symbol's location is in code.|  
|[IDiaSymbol::get_function](../vs140/IDiaSymbol--get_function.md)|`BOOL`|`TRUE` if the symbol is a function.|  
|[length](../vs140/IDiaSymbol--get_length.md)|`ULONGLONG`|Length of this symbol in bytes.|  
|[IDiaSymbol::get_lexicalParent](../vs140/IDiaSymbol--get_lexicalParent.md)|`IDiaSymbol*`|Symbol for the global scope.|  
|[lexicalParentId](../vs140/IDiaSymbol--get_lexicalParentId.md)|`DWORD`|ID of the lexical parent symbol.|  
|[IDiaSymbol::get_locationType](../vs140/IDiaSymbol--get_locationType.md)|`DWORD`|Public symbols have static locations; for details, see [Symbol Locations](../vs140/Symbol-Locations.md).|  
|[IDiaSymbol::get_managed](../vs140/IDiaSymbol--get_managed.md)|`BOOL`|`TRUE` if the symbol's location is in managed code.|  
|[IDiaSymbol::get_msil](../vs140/IDiaSymbol--get_msil.md)|`BOOL`|`TRUE` if the symbol's location is in Microsoft Intermediate Language (MSIL) code.|  
|[IDiaSymbol::get_name](../vs140/IDiaSymbol--get_name.md)|`BSTR`|The fully decorated name of the symbol.|  
|[IDiaSymbol::get_symIndexId Method](../vs140/IDiaSymbol--get_symIndexId.md)|`DWORD`|Index ID of symbol.|  
|[relativeVirtualAddress](../vs140/IDiaSymbol--get_relativeVirtualAddress.md)|`DWORD`|Relative position of the symbol within its block.|  
|[symTag](../vs140/IDiaSymbol--get_symTag.md)|`DWORD`|Returns `SymTagPublicSymbol` (one of the [SymTagEnum Enumeration](../vs140/SymTagEnum.md) values).|  
|[IDiaSymbol::get_undecoratedName](../vs140/IDiaSymbol--get_undecoratedName.md)|`BSTR`|The undecorated symbol name.|  
|[IDiaSymbol::get_undecoratedNameEx Method](../vs140/IDiaSymbol--get_undecoratedNameEx.md)|`BSTR`|Part or all of the undecorated symbol name.|  
  
## See Also  
 [Lexical Hierarchy of Symbol Types](../vs140/Lexical-Hierarchy-of-Symbol-Types.md)   
 [LocationType Enumeration](../vs140/LocationType.md)   
 [Symbol Locations](../vs140/Symbol-Locations.md)