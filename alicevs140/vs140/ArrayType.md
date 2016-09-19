---
title: "ArrayType"
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
ms.assetid: 1d973a3a-2bde-46df-8625-85d519bb3cc9
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ArrayType
An array is identified by a `SymTagArray` symbol.  
  
## Properties  
 The following table shows additional valid properties for this symbol type.  
  
|Property|Data type|Description|  
|--------------|---------------|-----------------|  
|[IDiaSymbol::get_arrayIndexType](../vs140/IDiaSymbol--get_arrayIndexType.md)|`IDiaSymbol*`|Symbol for the array index type.|  
|[arrayIndexTypeId](../vs140/IDiaSymbol--get_arrayIndexTypeId.md)|`DWORD`|ID of the array index type symbol.|  
|[constType](../vs140/IDiaSymbol--get_constType.md)|`BOOL`|`TRUE` if the array is marked as const.|  
|[count](../vs140/IDiaSymbol--get_count.md)|`DWORD`|Number of items in the array.|  
|[IDiaSymbol::get_length](../vs140/IDiaSymbol--get_length.md)|`LONGLONG`|Size, in bytes, of this array.|  
|[lexicalParent](../vs140/IDiaSymbol--get_lexicalParent.md)|`IDiaSymbol*`|Symbol of the enclosing compiland.|  
|[lexicalParentId](../vs140/IDiaSymbol--get_lexicalParentId.md)|`DWORD`|ID of the lexical parent symbol.|  
|[IDiaSymbol::get_rank](../vs140/IDiaSymbol--get_rank.md)|`DWORD`|Rank of a FORTRAN multidimensional array.|  
|[IDiaSymbol::get_symIndexId Method](../vs140/IDiaSymbol--get_symIndexId.md)|`DWORD`|Index ID of symbol.|  
|[symTag](../vs140/IDiaSymbol--get_symTag.md)|`DWORD`|Returns `SymTagArray` (one of the [SymTagEnum Enumeration](../vs140/SymTagEnum.md) values).|  
|[IDiaSymbol::get_type](../vs140/IDiaSymbol--get_type.md)|`IDiaSymbol*`|Symbol for the array element type.|  
|[typeId](../vs140/IDiaSymbol--get_typeId.md)|`DWORD`|ID of the array element type symbol.|  
|[unalignedType](../vs140/IDiaSymbol--get_unalignedType.md)|`BOOL`|`TRUE` if the array is unaligned|  
|[volatileType](../vs140/IDiaSymbol--get_volatileType.md)|`BOOL`|`TRUE` if the array is marked as volatile.|  
  
## See Also  
 [Class Hierarchy of Symbol Types](../vs140/Class-Hierarchy-of-Symbol-Types.md)   
 [Dimension](../vs140/Dimension.md)