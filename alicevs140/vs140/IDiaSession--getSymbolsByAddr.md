---
title: "IDiaSession::getSymbolsByAddr"
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
ms.assetid: eafcc757-b488-487d-a063-ad3703ff42e8
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaSession::getSymbolsByAddr
Retrieves an enumerator that finds symbols in the order of their addresses.  
  
## Syntax  
  
```cpp#  
HRESULT getSymbolsByAddr(   
   IDiaEnumSymbolsByAddr** ppEnumbyAddr  
);  
```  
  
#### Parameters  
 `ppEnumbyAddr`  
 [out] Returns an [IDiaEnumSymbolsByAddr](../vs140/IDiaEnumSymbolsByAddr.md) object. Use this interface to search for symbols in the symbol store by memory location.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## See Also  
 [IDiaSession](../vs140/IDiaSession.md)   
 [IDiaEnumSymbolsByAddr](../vs140/IDiaEnumSymbolsByAddr.md)