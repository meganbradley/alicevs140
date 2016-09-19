---
title: "IDiaLoadCallback::RestrictRegistryAccess"
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
ms.assetid: de4760c3-a746-4bab-8065-1388fed31b67
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaLoadCallback::RestrictRegistryAccess
Determines if registry queries can be used to locate symbol search paths.  
  
## Syntax  
  
```cpp#  
HRESULT RestrictRegistryAccess();  
```  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 Any return code other than `S_OK` prevents querying the registry for symbol search paths.  
  
## See Also  
 [IDiaLoadCallback2](../vs140/IDiaLoadCallback2.md)