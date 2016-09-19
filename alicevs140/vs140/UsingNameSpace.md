---
title: "UsingNameSpace"
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
ms.assetid: e8e1beb5-7cb9-43b4-9ff4-760d5f91ea2d
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# UsingNameSpace
Some symbols might be referred to by namespace, and would subsequently be identified by a `SymTagUsingNameSpace` tag.  
  
> [!NOTE]
>  The UsingNamespace symbol tag appears only in managed code.  
  
## Properties  
 The following table shows the properties that are valid for this symbol type.  
  
|Property|Data type|Description|  
|--------------|---------------|-----------------|  
|[IDiaSymbol::get_lexicalParent](../vs140/IDiaSymbol--get_lexicalParent.md)|`IDiaSymbol*`|Symbol for the enclosing compiland, block, or function.|  
|[lexicalParentId](../vs140/IDiaSymbol--get_lexicalParentId.md)|`DWORD`|ID of the lexical parent symbol.|  
|[IDiaSymbol::get_name](../vs140/IDiaSymbol--get_name.md)|`BSTR`|Namespace name.|  
|[IDiaSymbol::get_symIndexId Method](../vs140/IDiaSymbol--get_symIndexId.md)|`DWORD`|Index ID of symbol.|  
|[symTag](../vs140/IDiaSymbol--get_symTag.md)|`DWORD`|Returns `SymTagNameSpace` (one of the [SymTagEnum Enumeration](../vs140/SymTagEnum.md) values).|  
  
## See Also  
 [Lexical Hierarchy of Symbol Types](../vs140/Lexical-Hierarchy-of-Symbol-Types.md)