---
title: "IDiaSymbol::get_localBasePointerRegisterId"
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
ms.assetid: 9cbcaf00-9ace-45e1-b164-7a9439e08083
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaSymbol::get_localBasePointerRegisterId
Retrieves the ID of the register that holds a base pointer to local variables on the stack. Use when the [SymTagEnum](../vs140/SymTagEnum.md) is set to `SymTagFunction`.  
  
## Syntax  
  
```cpp#  
HRESULT get_localBasePointerRegisterId (   
   DWORD* pRetVal  
);  
```  
  
#### Parameters  
 `pRetVal`  
 [out] Returns the ID of the register that holds a base pointer to local variables on the stack.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns `S_FALSE` or an error code.  
  
> [!NOTE]
>  A return value of `S_FALSE` means the property is not available for the symbol.  
  
## Remarks  
  
## Requirements  
 Header: Dia2.h  
  
 Library: diaguids.lib  
  
 DLL: msdia100.dll  
  
## See Also  
 [IDiaSymbol](../vs140/IDiaSymbol.md)