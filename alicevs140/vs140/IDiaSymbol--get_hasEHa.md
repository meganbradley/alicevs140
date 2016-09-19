---
title: "IDiaSymbol::get_hasEHa"
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
ms.assetid: cb61dfd9-fe69-461c-8185-288440454864
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaSymbol::get_hasEHa
Retrieves a flag that specifies whether the function contains asynchronous (structured) exception handling.  
  
## Syntax  
  
```cpp  
HRESULT get_hasEHa(  
   BOOL *pFlag  
);  
```  
  
#### Parameters  
 `pFlag`  
 [out] Returns `TRUE` if the function has any asynchronous exception handling; otherwise, returns `FALSE`.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns `S_FALSE` or an error code.  
  
> [!NOTE]
>  A return value of `S_FALSE` means that the property is not available for the symbol.  
  
## Remarks  
 It is possible to mix asynchronous or structured exception handling with C++-style exception handling, but it requires a specific compiler switch, /EHa, to enable it.  
  
## Requirements  
  
|Requirement|Description|  
|-----------------|-----------------|  
|Header:|dia2.h|  
|Version:|DIA SDK v8.0|  
  
## See Also  
 [IDiaSymbol](../vs140/IDiaSymbol.md)