---
title: "BaseClass"
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
ms.assetid: 9375ca35-cb91-45f5-8903-7344ee4528e8
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# BaseClass
Each base class for a user-defined type (UDT) symbol is identified by a child with a `SymTagBaseClass` tag. The [type](../vs140/IDiaSymbol--get_type.md) property contains the symbol for the underlying UDT, and all properties of the underlying UDT are available as part of this BaseClass symbol.  
  
## Properties  
 The following table shows additional valid properties for this symbol type.  
  
|Property|Data type|Description|  
|--------------|---------------|-----------------|  
|[access](../vs140/IDiaSymbol--get_access.md)|`DWORD`|Access modifier applied to this base class. One of the [CV_access_e Enumeration](../vs140/CV_access_e.md) values.|  
|[classParent](../vs140/IDiaSymbol--get_classParent.md)|`IDiaSymbol*`|Symbol of the enclosing class (if any).|  
|[classParentId](../vs140/IDiaSymbol--get_classParentId.md)|`DWORD`|ID of the class parent symbol.|  
|[constructor](../vs140/IDiaSymbol--get_constructor.md)|`BOOL`|`TRUE` if the base class has a constructor.|  
|[constType](../vs140/IDiaSymbol--get_constType.md)|`BOOL`|`TRUE` if the base class is marked as const.|  
|[hasAssignmentOperator](../vs140/IDiaSymbol--get_hasAssignmentOperator.md)|`BOOL`|`TRUE` if the base class has an assignment operator.|  
|[hasCastOperator](../vs140/IDiaSymbol--get_hasCastOperator.md)|`BOOL`|`TRUE` if the base class has a cast operator.|  
|[hasNestedTypes](../vs140/IDiaSymbol--get_hasNestedTypes.md)|`BOOL`|`TRUE` if the base class has nested types.|  
|[IDiaSymbol::get_indirectVirtualBaseClass](../vs140/IDiaSymbol--get_indirectVirtualBaseClass.md)|`BOOL`|`TRUE` if the base class is indirect.|  
|[length](../vs140/IDiaSymbol--get_length.md)|`DWORD`|Length of this base class in bytes.|  
|[lexicalParent](../vs140/IDiaSymbol--get_lexicalParent.md)|`IDiaSymbol*`|Symbol of the enclosing compiland.|  
|[lexicalParentId](../vs140/IDiaSymbol--get_lexicalParentId.md)|`DWORD`|ID of the lexical parent symbol.|  
|[name](../vs140/IDiaSymbol--get_name.md)|`BSTR`|Name of the base class.|  
|[nested](../vs140/IDiaSymbol--get_nested.md)|`BOOL`|`TRUE` if the base class is nested.|  
|[IDiaSymbol::get_offset](../vs140/IDiaSymbol--get_offset.md)|`LONG`|Offset of subobject that represents the base class within the structure.|  
|[overloadedOperator](../vs140/IDiaSymbol--get_overloadedOperator.md)|`BOOL`|`TRUE` if the base class has any overloaded operators.|  
|[packed](../vs140/IDiaSymbol--get_packed.md)|`BOOL`|`TRUE` if the base class is packed.|  
|[scoped](../vs140/IDiaSymbol--get_scoped.md)|`BOOL`|`TRUE` if the base class appears in a nonglobal scope.|  
|[IDiaSymbol::get_symIndexId Method](../vs140/IDiaSymbol--get_symIndexId.md)|`DWORD`|Index ID of symbol.|  
|[symTag](../vs140/IDiaSymbol--get_symTag.md)|`DWORD`|Returns `SymTagBaseClass` (one of the [SymTagEnum Enumeration](../vs140/SymTagEnum.md) values).|  
|[IDiaSymbol::get_type](../vs140/IDiaSymbol--get_type.md)|`IDiaSymbol*`|The symbol for the base class [UDT](../vs140/UDT.md).|  
|[typeId](../vs140/IDiaSymbol--get_typeId.md)|`DWORD`|ID of the type symbol.|  
|[udtKind](../vs140/IDiaSymbol--get_udtKind.md)|`DWORD`|A value from the [UdtKind Enumeration](../vs140/UdtKind.md).|  
|[unalignedType](../vs140/IDiaSymbol--get_unalignedType.md)|`BOOL`|`TRUE` if the base class is unaligned.|  
|[IDiaSymbol::get_virtualBaseClass](../vs140/IDiaSymbol--get_virtualBaseClass.md)|`BOOL`|`TRUE` if the base class is virtual.|  
|[IDiaSymbol::get_virtualBaseDispIndex](../vs140/IDiaSymbol--get_virtualBaseDispIndex.md)|`DWORD`|Index into the virtual base displacement table.|  
|[IDiaSymbol::get_virtualBasePointerOffset](../vs140/IDiaSymbol--get_virtualBasePointerOffset.md)|`LONG`|Offset of the virtual base pointer.|  
|[virtualBaseTableType](../vs140/IDiaSymbol--get_virtualBaseTableType.md)|`IDiaSymbol*`|The type of the virtual base table pointer.|  
|[virtualTableShape](../vs140/IDiaSymbol--get_virtualTableShape.md)|`IDiaSymbol*`|The symbol describing the type of the virtual table for this base class.|  
|[virtualTableShapeId](../vs140/IDiaSymbol--get_virtualTableShapeId.md)|`DWORD`|ID of the virtual table shape symbol.|  
|[volatileType](../vs140/IDiaSymbol--get_volatileType.md)|`BOOL`|`TRUE` if the base class is marked as volatile.|  
  
## See Also  
 [Class Hierarchy of Symbol Types](../vs140/Class-Hierarchy-of-Symbol-Types.md)   
 [UDT](../vs140/UDT.md)