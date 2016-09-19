---
title: "Typedef (Debug Interface Access SDK)"
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
ms.assetid: 9ab441b9-cc72-47fa-83e2-87b3c2b891b4
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Typedef (Debug Interface Access SDK)
Symbols with `SymTagTypedef` tags introduce names for other types.  
  
## Properties  
 The following table shows additional valid properties for this symbol type.  
  
|Property|Data type|Description|  
|--------------|---------------|-----------------|  
|[baseType](../vs140/IDiaSymbol--get_baseType.md)|`DWORD`|One of the [BasicType Enumeration](../vs140/BasicType.md) values.|  
|[classParent](../vs140/IDiaSymbol--get_classParent.md)|`IDiaSymbol*`|Class parent of this typedef, if any.|  
|[classParentId](../vs140/IDiaSymbol--get_classParentId.md)|`DWORD`|ID of the class parent symbol.|  
|[constructor](../vs140/IDiaSymbol--get_constructor.md)|`BOOL`|`TRUE` if this typedef has a constructor.|  
|[constType](../vs140/IDiaSymbol--get_constType.md)|`BOOL`|`TRUE` if this typedef is marked as constant.|  
|[hasAssignmentOperator](../vs140/IDiaSymbol--get_hasAssignmentOperator.md)|`BOOL`|`TRUE` if this typedef has an assignment operator.|  
|[hasCastOperator](../vs140/IDiaSymbol--get_hasCastOperator.md)|`BOOL`|`TRUE` if this typedef has a cast operator.|  
|[hasNestedTypes](../vs140/IDiaSymbol--get_hasNestedTypes.md)|`BOOL`|`TRUE` if this typedef has nested types.|  
|[length](../vs140/IDiaSymbol--get_length.md)|`ULONGLONG`|Length of this typedef in bytes.|  
|[lexicalParent](../vs140/IDiaSymbol--get_lexicalParent.md)|`IDiaSymbol*`|Symbol of the enclosing compiland.|  
|[lexicalParentId](../vs140/IDiaSymbol--get_lexicalParentId.md)|`DWORD`|ID of the lexical parent symbol.|  
|[IDiaSymbol::get_name](../vs140/IDiaSymbol--get_name.md)|`BSTR`|Name of the typedef.|  
|[nested](../vs140/IDiaSymbol--get_nested.md)|`BOOL`|`TRUE` if this typedef is nested in a lexical scope.|  
|[overloadedOperator](../vs140/IDiaSymbol--get_overloadedOperator.md)|`BOOL`|`TRUE` if this typedef has an overloaded operator.|  
|[packed](../vs140/IDiaSymbol--get_packed.md)|`BOOL`|`TRUE` if this typedef is packed.|  
|[reference](../vs140/IDiaSymbol--get_reference.md)|`BOOL`|`TRUE` if this typedef is a reference.|  
|[scoped](../vs140/IDiaSymbol--get_scoped.md)|`BOOL`|`TRUE` if this typedef is in a nonglobal lexical scope.|  
|[IDiaSymbol::get_symIndexId Method](../vs140/IDiaSymbol--get_symIndexId.md)|`DWORD`|Index ID of symbol.|  
|[symTag](../vs140/IDiaSymbol--get_symTag.md)|`DWORD`|Returns `SymTagTypedef` (one of the [SymTagEnum Enumeration](../vs140/SymTagEnum.md) values).|  
|[IDiaSymbol::get_type](../vs140/IDiaSymbol--get_type.md)|`IDiaSymbol*`|Symbol for the underlying type.|  
|[typeId](../vs140/IDiaSymbol--get_typeId.md)|`DWORD`|ID of the type symbol.|  
|[udtKind](../vs140/IDiaSymbol--get_udtKind.md)|`DWORD`|One of the [UdtKind Enumeration](../vs140/UdtKind.md) values.|  
|[unalignedType](../vs140/IDiaSymbol--get_unalignedType.md)|`BOOL`|`TRUE` if this typedef is not aligned.|  
|[virtualTableShape](../vs140/IDiaSymbol--get_virtualTableShape.md)|`IDiaSymbol*`|The symbol that describes the virtual table shape.|  
|[virtualTableShapeId](../vs140/IDiaSymbol--get_virtualTableShapeId.md)|`DWORD`|ID of the virtual table shape symbol.|  
|[volatileType](../vs140/IDiaSymbol--get_volatileType.md)|`BOOL`|`TRUE` if this typedef is marked as volatile.|  
  
## Remarks  
 Since a typedef can represent a class, pointer, or user-defined type (UDT), the symbol for a typedef shares the same properties as one of those other types of symbols.  
  
## See Also  
 [Class Hierarchy of Symbol Types](../vs140/Class-Hierarchy-of-Symbol-Types.md)