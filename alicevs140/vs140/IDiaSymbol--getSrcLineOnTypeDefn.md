---
title: "IDiaSymbol::getSrcLineOnTypeDefn"
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
ms.assetid: ad554d18-9988-4b64-ad71-e7594c266e94
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaSymbol::getSrcLineOnTypeDefn
Retrieves the source file and line number that indicate where a specified user-defined type is defined.  
  
## Syntax  
  
```cpp  
HRESULT getSrcLineOnTypeDefn(  
   IDiaLineNumber **ppResult);  
```  
  
#### Parameters  
 `ppResult`  
 [out] A `IDiaLineNumber` object that contains the source file and line number where the user-defined.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns `S_FALSE` or an error code.  
  
## See Also  
 [IDiaSymbol](../vs140/IDiaSymbol.md)   
 [IDiaLineNumber](../vs140/IDiaLineNumber.md)