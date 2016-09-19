---
title: "IDiaLineNumber::get_lineNumberEnd"
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
ms.assetid: b101853e-2bcf-47c1-acef-e13984c7ea9d
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaLineNumber::get_lineNumberEnd
Retrieves the one-based source line number where the statement or expression ends.  
  
## Syntax  
  
```cpp#  
HRESULT get_lineNumberEnd (   
   DWORD* pRetVal  
);  
```  
  
#### Parameters  
 `pRetVal`  
 [out] Returns the line number where the statement or expression ends. If the value is zero, then the end information is not present.  
  
## Return Value  
 If successful, returns `S_OK`. Returns `S_FALSE` if this property is not supported. Otherwise, returns an error code.  
  
## See Also  
 [IDiaLineNumber](../vs140/IDiaLineNumber.md)