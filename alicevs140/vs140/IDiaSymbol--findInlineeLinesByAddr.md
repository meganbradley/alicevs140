---
title: "IDiaSymbol::findInlineeLinesByAddr"
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
ms.assetid: f1ab47ca-c851-48ea-9c12-47fb80b31102
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaSymbol::findInlineeLinesByAddr
Retrieves an enumeration that allows a client to iterate through the line number information of all functions that are inlined, directly or indirectly, in this symbol within the specified address range.  
  
## Syntax  
  
```cpp#  
HRESULT findInlineeLinesByAddr (   
   DWORD                 isect,  
   DWORD                 offset,  
   DWORD                 length,  
   IDiaEnumLineNumbers** ppResult  
);  
```  
  
#### Parameters  
 `isect`  
 [in] Specifies the section component of the address.  
  
 `offset`  
 [in] Specifies the offset component of the address.  
  
 `length`  
 [in] Specifies the address range, in number of bytes, to cover with this query.  
  
 `ppResult`  
 [out] Holds an `IDiaEnumLineNumbers` object that contains the list of line numbers that are retrieved.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## See Also  
 [IDiaSession](../vs140/IDiaSession.md)   
 [IDiaSymbol](../vs140/IDiaSymbol.md)   
 [SymTagEnum Enumeration](../vs140/SymTagEnum.md)   
 [IDiaEnumLineNumbers](../vs140/IDiaEnumLineNumbers.md)   
 [IDiaSession::findInlineeLines](../vs140/IDiaSession--findInlineeLines.md)