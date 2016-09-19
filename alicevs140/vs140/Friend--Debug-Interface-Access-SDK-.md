---
title: "Friend (Debug Interface Access SDK)"
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
ms.assetid: 5147a170-41ce-4727-8ace-c318e8d11647
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Friend (Debug Interface Access SDK)
Friend classes and friend functions are identified by `SymTagFriend` symbols. They are children of parent user-defined types (UDTs) and have a [classParent](../vs140/IDiaSymbol--get_classParent.md) property.  
  
## Properties  
 The following table shows additional valid properties for this symbol type.  
  
|Property|Data type|Description|  
|--------------|---------------|-----------------|  
|[IDiaSymbol::get_classParent](../vs140/IDiaSymbol--get_classParent.md)|`IDiaSymbol*`|Symbol for the UDT parent.|  
|[classParentId](../vs140/IDiaSymbol--get_classParentId.md)|`DWORD`|ID of the class parent symbol.|  
|[IDiaSymbol::get_name](../vs140/IDiaSymbol--get_name.md)|`BSTR`|Name of the class or function.|  
|[IDiaSymbol::get_symIndexId Method](../vs140/IDiaSymbol--get_symIndexId.md)|`DWORD`|Index ID of symbol.|  
|[symTag](../vs140/IDiaSymbol--get_symTag.md)|`DWORD`|Returns `SymTagFriend` (one of the [SymTagEnum Enumeration](../vs140/SymTagEnum.md) values).|  
|[IDiaSymbol::get_type](../vs140/IDiaSymbol--get_type.md)|`IDiaSymbol*`|Symbol for the class or function.|  
|[typeId](../vs140/IDiaSymbol--get_typeId.md)|`DWORD`|ID of the type symbol.|  
  
## See Also  
 [Class Hierarchy of Symbol Types](../vs140/Class-Hierarchy-of-Symbol-Types.md)