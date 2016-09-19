---
title: "FunctionType"
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
ms.assetid: 646a07e7-9d4f-4e21-95e3-3e403cdd4843
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# FunctionType
Each unique function signature is identified by a `SymTagFunctionType` symbol. Each parameter is identified as a class child symbol with a `SymTagFunctionArgType` tag.  
  
## Properties  
 The following table shows additional valid properties for this symbol type.  
  
|Property|Data type|Description|  
|--------------|---------------|-----------------|  
|[IDiaSymbol::get_callingConvention](../vs140/IDiaSymbol--get_callingConvention.md)|`DWORD`|One of the values of the [CV_call_e Enumeration](../vs140/CV_call_e.md).|  
|[IDiaSymbol::get_classParent](../vs140/IDiaSymbol--get_classParent.md)|`IDiaSymbol*`|Class that this function (or method) is a member of.|  
|[classParentId](../vs140/IDiaSymbol--get_classParentId.md)|`DWORD`|ID of the class parent symbol.|  
|[constType](../vs140/IDiaSymbol--get_constType.md)|`BOOL`|`TRUE` if the function is marked as constant.|  
|[IDiaSymbol::get_count](../vs140/IDiaSymbol--get_count.md)|`DWORD`|Number of function parameters.|  
|[lexicalParent](../vs140/IDiaSymbol--get_lexicalParent.md)|`IDiaSymbol*`|Symbol of the enclosing compiland.|  
|[lexicalParentId](../vs140/IDiaSymbol--get_lexicalParentId.md)|`DWORD`|ID of the lexical parent symbol.|  
|[IDiaSymbol::get_objectPointerType](../vs140/IDiaSymbol--get_objectPointerType.md)|`IDiaSymbol*`|Type of the method's object pointer ("this").|  
|[IDiaSymbol::get_symIndexId Method](../vs140/IDiaSymbol--get_symIndexId.md)|`DWORD`|Index ID of symbol.|  
|[symTag](../vs140/IDiaSymbol--get_symTag.md)|`DWORD`|Returns `SymTagFunctionType` (one of the [SymTagEnum Enumeration](../vs140/SymTagEnum.md) values).|  
|[IDiaSymbol::get_thisAdjust](../vs140/IDiaSymbol--get_thisAdjust.md)|`LONG`|Logical "this" adjustor for the method.|  
|[IDiaSymbol::get_type](../vs140/IDiaSymbol--get_type.md)|`IDiaSymbol*`|Symbol for the return value type.|  
|[typeId](../vs140/IDiaSymbol--get_typeId.md)|`DWORD`|ID of the type symbol.|  
|[unalignedType](../vs140/IDiaSymbol--get_unalignedType.md)|`BOOL`|`TRUE` if the function is unaligned.|  
|[volatileType](../vs140/IDiaSymbol--get_volatileType.md)|`BOOL`|`TRUE` if the function is marked as volatile.|  
  
## See Also  
 [Class Hierarchy of Symbol Types](../vs140/Class-Hierarchy-of-Symbol-Types.md)   
 [CV_access_e Enumeration](../vs140/CV_access_e.md)   
 [FunctionArgType](../vs140/FunctionArgType.md)