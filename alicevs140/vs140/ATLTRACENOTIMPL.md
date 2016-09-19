---
title: "ATLTRACENOTIMPL"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: 1ee1bede-3f30-49b1-bc52-87672cb5e296
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ATLTRACENOTIMPL
In debug builds of ATL, sends the string "`funcname` is not implemented" to the dump device and returns **E_NOTIMPL**.  
  
## Syntax  
  
```  
  
ATLTRACENOTIMPL( funcname );  
```  
  
#### Parameters  
 `funcname`  
 [in] A string containing the name of the function that is not implemented.  
  
## Remarks  
 In release builds, simply returns **E_NOTIMPL**.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#127](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#127)]  
  
## Requirements  
 **Header:** atltrace.h  
  
## See Also  
 [Debugging and Error Reporting Macros](../vs140/Debugging-and-Error-Reporting-Macros.md)   
 [Macros](../vs140/ATL-Macros.md)   
 [ATLTRACE2](../vs140/ATLTRACE2.md)