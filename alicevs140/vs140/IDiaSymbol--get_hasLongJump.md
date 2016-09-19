---
title: "IDiaSymbol::get_hasLongJump"
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
ms.assetid: 14484cb1-43b0-47a1-a9a8-081b55566886
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaSymbol::get_hasLongJump
Retrieves a flag that specifies whether the function contains a use of the [longjmp](../vs140/longjmp.md) command (paired with a [setjmp](../vs140/setjmp.md) command, these form the C-style method of exception handling).  
  
## Syntax  
  
```cpp#  
HRESULT get_hasLongJump  
   BOOL *pFlag  
);  
```  
  
#### Parameters  
 `pFlag`  
 [out] Returns `TRUE` if the function contains a `longjmp` command; otherwise, returns `FALSE`.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns `S_FALSE` or an error code.  
  
> [!NOTE]
>  A return value of `S_FALSE` means that the property is not available for the symbol.  
  
## Requirements  
  
|Requirement|Description|  
|-----------------|-----------------|  
|Header:|dia2.h|  
|Version:|DIA SDK v8.0|  
  
## See Also  
 [IDiaSymbol Interface](../vs140/IDiaSymbol.md)   
 [IDiaSymbol::get_hasSetJump Method](../vs140/IDiaSymbol--get_hasSetJump.md)   
 [longjmp](../vs140/longjmp.md)   
 [setjmp](../vs140/setjmp.md)