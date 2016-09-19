---
title: "IDiaSymbol::get_packed"
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
ms.assetid: e42ff368-56c4-49a2-8676-f80e349efa21
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaSymbol::get_packed
Retrieves a flag that specifies whether the user-defined data type (UDT) is packed.  
  
## Syntax  
  
```cpp#  
HRESULT get_packed (   
   BOOL* pRetVal  
);  
```  
  
#### Parameters  
 `pRetVal`  
 [out] Returns `TRUE` if the UDT is packed; otherwise, returns `FALSE`.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns `S_FALSE` or an error code.  
  
> [!NOTE]
>  A return value of `S_FALSE` means that the property is not available for the symbol.  
  
## Remarks  
 Packed means all the members of the UDT are positioned as close together as possible, with no intervening padding to align to memory boundaries.  
  
## See Also  
 [IDiaSymbol](../vs140/IDiaSymbol.md)