---
title: "IDiaSymbol::get_baseDataSlot"
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
ms.assetid: f9ed21b7-9397-4813-926e-ade11914b06b
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaSymbol::get_baseDataSlot
Retrieves the base data slot.  
  
## Syntax  
  
```cpp  
HRESULT get_baseDataSlot(   
   DWORD* pRetVal);  
```  
  
#### Parameters  
 `pRetVal`  
 [out] A pointer to a `DWORD` that holds the base data slot.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns `S_FALSE` or an error code.  
  
## See Also  
 [IDiaSymbol](../vs140/IDiaSymbol.md)