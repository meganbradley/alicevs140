---
title: "IDiaSymbol::get_hasSetJump"
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
ms.assetid: 22656206-dccf-40ed-b179-fc016d1b262a
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaSymbol::get_hasSetJump
Retrieves a flag that specifies whether the function contains a use of the [setjmp](../vs140/setjmp.md) command (paired with the [longjmp](../vs140/longjmp.md) command, these form the C-style method of exception handling).  
  
## Syntax  
  
```cpp  
HRESULT get_hasSetJump(  
   BOOL *pFlag  
);  
```  
  
#### Parameters  
 `pFlag`  
 [out] Returns `TRUE` if the function contains a `setjmp` command; otherwise, returns `FALSE`.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns `S_FALSE` or error code.  
  
> [!NOTE]
>  A return value of `S_FALSE` means the property is not available for the symbol.  
  
## Requirements  
  
|Requirement|Description|  
|-----------------|-----------------|  
|Header:|dia2.h|  
|Version:|DIA SDK v8.0|  
  
## See Also  
 [IDiaSymbol](../vs140/IDiaSymbol.md)   
 [IDiaSymbol::get_hasLongJump](../vs140/IDiaSymbol--get_hasLongJump.md)   
 [longjmp](../vs140/longjmp.md)   
 [setjmp](../vs140/setjmp.md)