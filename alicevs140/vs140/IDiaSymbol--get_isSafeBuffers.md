---
title: "IDiaSymbol::get_isSafeBuffers"
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
ms.assetid: f29e373d-e7bb-4181-ab9f-bf708d401d83
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaSymbol::get_isSafeBuffers
Retrieves a flag that specifies whether the preprocesser directive for a safe buffer is used. Use when the [SymTagEnum](../vs140/SymTagEnum.md) is set to `SymTagFunction`.  
  
## Syntax  
  
```cpp#  
HRESULT get_isSafeBuffers(   
   BOOL* pRetVal)  
);  
```  
  
#### Parameters  
 `pRetVal`  
 [out] Returns `TRUE` if the pointer uses a preprocessor directive for a safe buffer; otherwise, returns `FALSE`.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns `S_FALSE` or an error code.  
  
> [!NOTE]
>  A return value of `S_FALSE` means the property is not available for the symbol.  
  
## Remarks  
  
## Requirements  
 Header: Dia2.h  
  
 Library: diaguids.lib  
  
 DLL: msdia100.dll  
  
## See Also  
 [IDiaSymbol](../vs140/IDiaSymbol.md)   
 [strict_gs_check](../vs140/strict_gs_check.md)