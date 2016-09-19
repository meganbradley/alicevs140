---
title: "IDiaSession::findSymbolByToken"
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
ms.assetid: 3c92149c-6eef-454f-86be-66e89557b9e6
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaSession::findSymbolByToken
Retrieves the symbol that contains a specified metadata token.  
  
## Syntax  
  
```cpp#  
HRESULT findSymbolByToken (   
   ULONG        token,  
   SymTagEnum   symtag,  
   IDiaSymbol** ppSymbol  
);  
```  
  
#### Parameters  
 `token`  
 [in] Specifies the token.  
  
 `symtag`  
 [in] Symbol type to be found. Values are taken from the [SymTagEnum Enumeration](../vs140/SymTagEnum.md) enumeration.  
  
 `ppSymbol`  
 [out] Returns an [IDiaSymbol](../vs140/IDiaSymbol.md) object that represents the symbol retrieved.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Example  
  
```cpp#  
IDiaSymbol* pFunc;  
pSession->findSymbolByToken( token, SymTagFunction, &pFunc );  
```  
  
## See Also  
 [IDiaSession](../vs140/IDiaSession.md)   
 [IDiaSymbol](../vs140/IDiaSymbol.md)   
 [SymTagEnum Enumeration](../vs140/SymTagEnum.md)