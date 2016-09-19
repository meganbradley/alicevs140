---
title: "IDiaSymbol::get_targetVirtualAddress"
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
ms.assetid: a0a5ce72-95f8-443e-bb4b-8c21194faad0
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaSymbol::get_targetVirtualAddress
Retrieves the virtual address (VA) of a thunk target.  
  
## Syntax  
  
```cpp#  
HRESULT get_targetVirtualAddress (   
   ULONGLONG* pRetVal  
);  
```  
  
#### Parameters  
 `pRetVal`  
 [out] Returns the VA of a thunk target.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns `S_FALSE` or an error code.  
  
> [!NOTE]
>  A return value of `S_FALSE` means the property is not available for the symbol.  
  
## Remarks  
 This property is valid only if the symbol as a [SymTagEnum](../vs140/SymTagEnum.md) value of `SymTagThunk`.  
  
 A "thunk" is a piece of code that converts between a 32-bit memory address space (also known as flat address space) and a 16-bit address space (known as a segmented address space).  
  
## See Also  
 [IDiaSymbol](../vs140/IDiaSymbol.md)   
 [SymTagEnum](../vs140/SymTagEnum.md)