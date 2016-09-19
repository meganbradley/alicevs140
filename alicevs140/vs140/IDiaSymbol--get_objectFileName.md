---
title: "IDiaSymbol::get_objectFileName"
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
ms.assetid: 21793872-4879-4e4d-b527-dcf70aa7fb31
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaSymbol::get_objectFileName
Retrieves the object file name.  
  
## Syntax  
  
```cpp  
HRESULT get_objectFilename(   
   BSTR *pRetVal);  
```  
  
#### Parameters  
 `pRetVal`  
 [out] A pointer to a `BSTR` that holds the object file name.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns `S_FALSE` or an error code.  
  
## See Also  
 [IDiaSymbol](../vs140/IDiaSymbol.md)