---
title: "IDiaSymbol::get_managed"
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
ms.assetid: a69d00be-2a89-415c-b116-385c422e2fd5
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaSymbol::get_managed
Retrieves a flag that specifies whether the symbol refers to managed code.  
  
## Syntax  
  
```cpp#  
HRESULT get_managed (   
   BOOL* pRetVal  
);  
```  
  
#### Parameters  
 `pRetVal`  
 [out] Returns `TRUE` if the symbol refers to managed code; otherwise, returns `FALSE`.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns `S_FALSE` or an error code.  
  
> [!NOTE]
>  A return value of `S_FALSE` means the property is not available for the symbol.  
  
## See Also  
 [IDiaSymbol](../vs140/IDiaSymbol.md)