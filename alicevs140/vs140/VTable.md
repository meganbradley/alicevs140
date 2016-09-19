---
title: "VTable"
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
ms.assetid: c8be6692-7d2a-4721-99d3-8e2e565bb8a1
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# VTable
The virtual table is identified by the `SymTagVTable` symbol.  
  
## Properties  
 The following table shows additional valid properties for this symbol type.  
  
|Property|Data type|Description|  
|--------------|---------------|-----------------|  
|[classParent](../vs140/IDiaSymbol--get_classParent.md)|`IDiaSymbol*`|Symbol of the class that owns this VTable.|  
|[classParentId](../vs140/IDiaSymbol--get_classParentId.md)|`DWORD`|ID of the class parent symbol.|  
|[constType](../vs140/IDiaSymbol--get_constType.md)|`BOOL`|`TRUE` if the class of the VTable is marked as a constant.|  
|[lexicalParent](../vs140/IDiaSymbol--get_lexicalParent.md)|`IDiaSymbol*`|Symbol of the enclosing compiland.|  
|[lexicalParentId](../vs140/IDiaSymbol--get_lexicalParentId.md)|`DWORD`|ID of the lexical parent symbol.|  
|[IDiaSymbol::get_symIndexId Method](../vs140/IDiaSymbol--get_symIndexId.md)|`DWORD`|Index ID of symbol.|  
|[symTag](../vs140/IDiaSymbol--get_symTag.md)|`DWORD`|Returns `SymTagVTable` (one of the [SymTagEnum Enumeration](../vs140/SymTagEnum.md) values).|  
|[IDiaSymbol::get_type](../vs140/IDiaSymbol--get_type.md)|`IDiaSymbol*`|Symbol for the VTable's [VTableShape](../vs140/VTableShape.md).|  
|[typeId](../vs140/IDiaSymbol--get_typeId.md)|`DWORD`|ID of the type symbol.|  
|[unalignedType](../vs140/IDiaSymbol--get_unalignedType.md)|`BOOL`|`TRUE` if the class of the VTable is unaligned.|  
|[volatileType](../vs140/IDiaSymbol--get_volatileType.md)|`BOOL`|`TRUE` if the class of the VTable is marked as volatile.|  
  
## See Also  
 [Class Hierarchy of Symbol Types](../vs140/Class-Hierarchy-of-Symbol-Types.md)   
 [VTableShape](../vs140/VTableShape.md)