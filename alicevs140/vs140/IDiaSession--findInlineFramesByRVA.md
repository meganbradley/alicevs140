---
title: "IDiaSession::findInlineFramesByRVA"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ddb3ff0e-cb3d-4fa0-af56-f064b218b264
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaSession::findInlineFramesByRVA
Retrieves an enumeration that allows a client to iterate through all of the inline frames on a specified relative virtual address (RVA).  
  
## Syntax  
  
```cpp#  
HRESULT findInlineFramesByRVA (   
   IDiaSymbol*       parent,   DWORD             rva,  
   IDiaEnumSymbols** ppResult  
);  
```  
  
#### Parameters  
 `parent`  
 [in] An `IDiaSymbol` object representing the parent.  
  
 `rva`  
 [in] Specifies the address as an RVA.  
  
 `ppResult`  
 [out] Holds an `IDiaEnumSymbols` object that contains the list of frames that are retrieved.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## See Also  
 [IDiaSession](../vs140/IDiaSession.md)   
 [IDiaSymbol](../vs140/IDiaSymbol.md)   
 [SymTagEnum Enumeration](../vs140/SymTagEnum.md)   
 [IDiaEnumSymbols](../vs140/IDiaEnumSymbols.md)