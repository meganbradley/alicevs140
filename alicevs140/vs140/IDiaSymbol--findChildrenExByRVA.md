---
title: "IDiaSymbol::findChildrenExByRVA"
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
ms.assetid: cbc57c6c-7d64-4469-a114-1dd6671e5ec5
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaSymbol::findChildrenExByRVA
Retrieves the children of the symbol that are valid at a specified relative virtual address (RVA).  
  
## Syntax  
  
```cpp#  
HRESULT findChildrenExByRVA (   
   enum SymTagEnum   symtag,  
   LPCOLESTR         name,  
   DWORD             compareFlags,  
   DWORD             address,  
   IDiaEnumSymbols** ppResult  
);  
```  
  
#### Parameters  
 `symtag`  
 [in] Specifies the symbol tags of the children to be retrieved, as defined in the [SymTagEnum Enumeration](../vs140/SymTagEnum.md). Set to `SymTagNull` for all children to be retrieved.  
  
 `name`  
 [in] Specifies the name of the children to be retrieved. Set to `NULL` for all children to be retrieved.  
  
 `compareFlags`  
 [in] Specifies the comparison options to be applied to name matching. Values from the [NameSearchOptions Enumeration](../vs140/NameSearchOptions.md) enumeration can be used alone or in combination.  
  
 `address`  
 [in] Specifies the RVA.  
  
 `ppResult`  
 [out] Returns an [IDiaEnumSymbols](../vs140/IDiaEnumSymbols.md) object that contains a list of the child symbols retrieved.  
  
## Return Value  
 Returns `S_OK` if at least one child of the symbol was found, or returns `S_FALSE` if no children were found; otherwise, returns an error code.  
  
## Remarks  
 The local symbols that are returned include live range information.  
  
## Requirements  
 Header: Dia2.h  
  
 Library: diaguids.lib  
  
 DLL: msdia100.dll  
  
## See Also  
 [IDiaSymbol](../vs140/IDiaSymbol.md)   
 [SymTagEnum Enumeration](../vs140/SymTagEnum.md)   
 [IDiaEnumSymbols](../vs140/IDiaEnumSymbols.md)   
 [IDiaSession::findChildren](../vs140/IDiaSession--findChildren.md)   
 [NameSearchOptions Enumeration](../vs140/NameSearchOptions.md)