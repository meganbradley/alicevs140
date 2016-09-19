---
title: "AtlGetVersion"
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
ms.assetid: 415804f6-64ba-417f-8937-bb4ae96540bb
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AtlGetVersion
Call this function to get the version of the ATL library that you are using.  
  
## Syntax  
  
```  
ATLAPI_(DWORD) AtlGetVersion(void* pReserved);  
```  
  
#### Parameters  
 `pReserved`  
 A reserved pointer.  
  
## Return Value  
 Returns a `DWORD` integer value of the version of the ATL library that you are compiling or running.  
  
## Example  
 The function should be called as follows.  
  
 [!CODE [NVC_ATL_Utilities#95](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#95)]  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [ATL Functions Alphabetical Reference](../vs140/ATL-Functions-Alphabetical-Reference.md)