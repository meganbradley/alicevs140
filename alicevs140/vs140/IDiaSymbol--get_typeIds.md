---
title: "IDiaSymbol::get_typeIds"
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
ms.assetid: 5166e647-fde5-4efe-92bf-77f8ae3fbc9b
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaSymbol::get_typeIds
Retrieves an array of compiler-specific type identifier values for this symbol.  
  
## Syntax  
  
```cpp#  
HRESULT get_typeIds (   
   DWORD  cTypeIds,  
   DWORD* pcTypeIds,  
   DWORD  typeIds[]  
);  
```  
  
#### Parameters  
 `cTypeIds`  
 [in] Size of the buffer to hold the data.  
  
 `pcTypeIds`  
 [out] Returns the number of `typeIds` written, or, if `typeIds` is `NULL`, then the total number of type identifiers available.  
  
 `typeIds[]`  
 [out] An array that is to be filled in with the type identifiers.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns `S_FALSE` or an error code.  
  
> [!NOTE]
>  A return value of `S_FALSE` means the property is not available for the symbol.  
  
## See Also  
 [IDiaSymbol](../vs140/IDiaSymbol.md)