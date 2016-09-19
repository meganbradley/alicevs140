---
title: "IDiaSymbol::get_dataKind"
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
ms.assetid: 45005ad0-8b29-4cde-9d33-6bef72f6e463
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaSymbol::get_dataKind
Retrieves the variable classification of a data symbol.  
  
## Syntax  
  
```cpp#  
HRESULT get_dataKind (   
   DWORD* pRetVal  
);  
```  
  
#### Parameters  
 `pRetVal`  
 [out] Returns a value from the [DataKind Enumeration](../vs140/DataKind.md) enumeration specifying the kind of data such as global, static, or constant, for example.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns `S_FALSE` or an error code.  
  
> [!NOTE]
>  A return value of `S_FALSE` means that the property is not available for the symbol.  
  
## Requirements  
  
|Requirement|Description|  
|-----------------|-----------------|  
|Header:|dia2.h|  
|Version:|DIA SDK v7.0|  
  
## See Also  
 [IDiaSymbol](../vs140/IDiaSymbol.md)   
 [DataKind Enumeration](../vs140/DataKind.md)