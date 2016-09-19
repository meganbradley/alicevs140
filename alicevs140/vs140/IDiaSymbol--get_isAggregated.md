---
title: "IDiaSymbol::get_isAggregated"
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
ms.assetid: 24d280ef-6ea3-4958-9418-4ad3ca7c67c1
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaSymbol::get_isAggregated
Retrieves a flag that specifies whether the data symbol is part of an aggregate or collection of symbols; the compiler will treat aggregated symbols as separate entities, but they are really part of a single larger symbol.  
  
## Syntax  
  
```cpp#  
HRESULT get_isAggregated(  
   BOOL *pFlag  
);  
```  
  
#### Parameters  
 `pFlag`  
 [out] Returns `TRUE` if the data is part of an aggregation of symbols split from a parent symbol; otherwise, returns `FALSE`.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns `S_FALSE` or an error code.  
  
> [!NOTE]
>  A return value of `S_FALSE` means the property is not available for the symbol.  
  
## Remarks  
 The [IDiaSymbol::get_isSplitted](../vs140/IDiaSymbol--get_isSplitted.md) method is `TRUE` for the symbol that is the parent of the aggregated symbols.  
  
## Requirements  
  
|Requirement|Description|  
|-----------------|-----------------|  
|Header:|dia2.h|  
|Version:|DIA SDK v8.0|  
  
## See Also  
 [IDiaSymbol](../vs140/IDiaSymbol.md)   
 [IDiaSymbol::get_isSplitted](../vs140/IDiaSymbol--get_isSplitted.md)