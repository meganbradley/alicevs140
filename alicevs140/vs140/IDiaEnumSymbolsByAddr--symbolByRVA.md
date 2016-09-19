---
title: "IDiaEnumSymbolsByAddr::symbolByRVA"
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
ms.assetid: f7828029-f2ee-4ccd-afac-785adc60a4c8
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaEnumSymbolsByAddr::symbolByRVA
Positions the enumerator by performing a lookup by relative virtual address (RVA).  
  
## Syntax  
  
```cpp#  
HRESULT symbolByRVA (   
   DWORD**      relativeVirtualAddress,  
   IDiaSymbol** ppsymbol  
);  
```  
  
#### Parameters  
 relativeVirtualAddress  
 [in] Address relative to start of image.  
  
 ppsymbol  
 [out] Returns an [IDiaSymbol](../vs140/IDiaSymbol.md) object representing the symbol found.  
  
## Return Value  
 If successful, returns `S_OK`. Returns `S_FALSE` if the symbol could not be found. Otherwise, returns an error code.  
  
## See Also  
 [IDiaEnumSymbolsByAddr](../vs140/IDiaEnumSymbolsByAddr.md)   
 [IDiaEnumSymbolsByAddr::symbolByVA](../vs140/IDiaEnumSymbolsByAddr--symbolByVA.md)   
 [IDiaSymbol](../vs140/IDiaSymbol.md)