---
title: "IDiaSymbol::get_hasSEH"
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
ms.assetid: 1a709ded-22c8-464c-97be-eba5e464210c
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaSymbol::get_hasSEH
Retrieves a flag that specifies whether the function contains any [Structured Exception Handling (C++)](../vs140/Structured-Exception-Handling--C-C---.md) (for example, __try/\__except blocks).  
  
## Syntax  
  
```cpp#  
HRESULT get_hasSEH(  
   BOOL *pFlag  
);  
```  
  
#### Parameters  
 `pFlag`  
 [out] Returns `TRUE` if the function has any structured exception handling blocks; otherwise, returns `FALSE`.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns `S_FALSE` or error code.  
  
> [!NOTE]
>  A return value of `S_FALSE` means the property is not available for the symbol.  
  
## Requirements  
  
|Requirement|Description|  
|-----------------|-----------------|  
|Header:|dia2.h|  
|Version:|DIA SDK v8.0|  
  
## See Also  
 [IDiaSymbol](../vs140/IDiaSymbol.md)   
 [Structured Exception Handling (C++)](../vs140/Structured-Exception-Handling--C-C---.md)