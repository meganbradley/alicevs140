---
title: "IDiaSymbol::get_isSplitted"
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
ms.assetid: ff160cf6-003b-4ef5-a406-20a7b287b2bf
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaSymbol::get_isSplitted
Retrieves a flag that specifies whether the data symbol has been split into an aggregation or collection of other symbols; the compiler treats the symbols as separate entities, even though they are really part of a larger symbol.  
  
## Syntax  
  
```cpp  
HRESULT get_isSplitted(  
   BOOL *pFlag  
);  
```  
  
#### Parameters  
 `pFlag`  
 [out] Returns `TRUE` if the symbol has been split into an aggregate of symbols; otherwise, returns `FALSE`.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns `S_FALSE` or error code.  
  
> [!NOTE]
>  A return value of `S_FALSE` means the property is not available for the symbol.  
  
## Remarks  
 The [IDiaSymbol::get_isAggregated](../vs140/IDiaSymbol--get_isAggregated.md) method returns `TRUE` for all symbols that are part of a split symbol.  
  
## Requirements  
  
|Requirement|Description|  
|-----------------|-----------------|  
|Header:|dia2.h|  
|Version:|DIA SDK v8.0|  
  
## See Also  
 [IDiaSymbol](../vs140/IDiaSymbol.md)   
 [IDiaSymbol::get_isAggregated](../vs140/IDiaSymbol--get_isAggregated.md)