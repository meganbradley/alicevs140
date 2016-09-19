---
title: "IDiaSymbol::get_container"
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
ms.assetid: 24e832eb-80b3-484c-a41b-11477ec9de99
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaSymbol::get_container
This function retrieves a pointer to a symbol representing the parent/container of this symbol.  
  
## Syntax  
  
```cpp#  
HRESULT get_container(  
   IDiaSymbol **pRetVal  
);  
```  
  
#### Parameters  
 `pRetVal`  
 [out] Returns a pointer to an `IDiaSymbol` containing information about the container of this symbol.  
  
## Return Value  
 If successful, returns S_OK; otherwise, returns S_FALSE or an error code.  
  
> [!NOTE]
>  A return value of S_FALSE means that the property is not available for the symbol.  
  
## Requirements  
  
|Requirement|Description|  
|-----------------|-----------------|  
|Header:|dia2.h|  
|Version:|DIA SDK v8.0|  
  
## See Also  
 [IDiaSymbol Interface](../vs140/IDiaSymbol.md)