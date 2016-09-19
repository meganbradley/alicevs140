---
title: "IDiaSymbol::get_rank"
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
ms.assetid: 14cc9c4b-a5ec-414a-b01f-4a142c17b7cc
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaSymbol::get_rank
Retrieves the rank (number of dimensions) of a FORTRAN multi-dimensional array.  
  
## Syntax  
  
```cpp#  
HRESULT get_rank (   
   DWORD* pRetVal  
);  
```  
  
#### Parameters  
 `pRetVal`  
 [out] Returns the number of dimensions in a FORTRAN multi-dimensional array.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns `S_FALSE` or an error code.  
  
> [!NOTE]
>  A return value of `S_FALSE` means the property is not available for the symbol.  
  
## Remarks  
 Rank refers to the number of dimensions in an array where the array is declared as `myarray[1,2,3]`. This example has a rank of 3 and 3 dimensions. Rank does not apply to C++ which uses the concept of an array of arrays for each dimension (that is, `myarray[1][2][3]`).  
  
## See Also  
 [IDiaSymbol](../vs140/IDiaSymbol.md)