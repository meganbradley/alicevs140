---
title: "Enum (Debug Interface Access SDK)"
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
ms.assetid: c777e2e6-88be-435b-b632-8d43f42b0b49
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Enum (Debug Interface Access SDK)
Enumerations are identified by `SymTagEnum` symbols. Each enumeration value appears as a class child with a `SymTagConstant` tag.  
  
## Properties  
 The following table shows additional valid properties for this symbol type.  
  
|Property|Data type|Description|  
|--------------|---------------|-----------------|  
|[baseType](../vs140/IDiaSymbol--get_baseType.md)|`DWORD`|One of the [BasicType Enumeration](../vs140/BasicType.md) values.|  
|[classParent](../vs140/IDiaSymbol--get_classParent.md)|`IDiaSymbol*`|Class parent of this enumeration, if any.|  
|[classParentId](../vs140/IDiaSymbol--get_classParentId.md)|`DWORD`|ID of the class parent symbol.|  
|[constructor](../vs140/IDiaSymbol--get_constructor.md)|`BOOL`|`TRUE` if the enumeration has a constructor.|  
|[constType](../vs140/IDiaSymbol--get_constType.md)|`BOOL`|`TRUE` if the enumeration is marked as const.|  
|[hasAssignmentOperator](../vs140/IDiaSymbol--get_hasAssignmentOperator.md)|`BOOL`|`TRUE` if the enumeration has an assignment operator.|  
|[hasCastOperator](../vs140/IDiaSymbol--get_hasCastOperator.md)|`BOOL`|`TRUE` if the enumeration has a cast operator.|  
|[hasNestedTypes](../vs140/IDiaSymbol--get_hasNestedTypes.md)|`BOOL`|`TRUE` if the enumeration has nested types.|  
|[length](../vs140/IDiaSymbol--get_length.md)|`DWORD`|Length of this enumeration in bytes.|  
|[lexicalParent](../vs140/IDiaSymbol--get_lexicalParent.md)|`IDiaSymbol*`|Symbol of the enclosing [Compiland](../vs140/Compiland.md).|  
|[lexicalParentId](../vs140/IDiaSymbol--get_lexicalParentId.md)|`DWORD`|ID of the lexical parent symbol.|  
|[IDiaSymbol::get_name](../vs140/IDiaSymbol--get_name.md)|`BSTR`|Name of the enumerated type.|  
|[IDiaSymbol::get_nested](../vs140/IDiaSymbol--get_nested.md)|`BOOL`|`TRUE` if the enumeration is nested.|  
|[overloadedOperator](../vs140/IDiaSymbol--get_overloadedOperator.md)|`BOOL`|`TRUE` if the enumeration has any overloaded operators.|  
|[packed](../vs140/IDiaSymbol--get_packed.md)|`BOOL`|`TRUE` if the enumeration is packed.|  
|[IDiaSymbol::get_scoped](../vs140/IDiaSymbol--get_scoped.md)|`BOOL`|`TRUE` if the enumeration appears in a nonglobal lexical scope.|  
|[IDiaSymbol::get_symIndexId Method](../vs140/IDiaSymbol--get_symIndexId.md)|`DWORD`|Index ID of symbol.|  
|[symTag](../vs140/IDiaSymbol--get_symTag.md)|`DWORD`|Returns `SymTagEnum` (one of the [SymTagEnum Enumeration](../vs140/SymTagEnum.md) values).|  
|[IDiaSymbol::get_type](../vs140/IDiaSymbol--get_type.md)|`IDiaSymbol*`|Symbol for the underlying type.|  
|[typeId](../vs140/IDiaSymbol--get_typeId.md)|`DWORD`|ID of the type symbol.|  
|[unalignedType](../vs140/IDiaSymbol--get_unalignedType.md)|`BOOL`|`TRUE` if the enumeration is unaligned.|  
|[volatileType](../vs140/IDiaSymbol--get_volatileType.md)|`BOOL`|`TRUE` if the enumeration is marked as volatile.|  
  
## See Also  
 [Class Hierarchy of Symbol Types](../vs140/Class-Hierarchy-of-Symbol-Types.md)