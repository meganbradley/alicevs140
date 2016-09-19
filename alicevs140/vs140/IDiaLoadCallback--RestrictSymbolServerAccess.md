---
title: "IDiaLoadCallback::RestrictSymbolServerAccess"
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
ms.assetid: db37ad9f-f75e-4f0c-83bf-21a6e66ba859
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaLoadCallback::RestrictSymbolServerAccess
Determines if access is allowed to a symbol server to resolve symbols.  
  
## Syntax  
  
```cpp#  
HRESULT RestrictSymbolServerAccess();  
```  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 Any return code other than `S_OK` prevents use of a symbol server to resolve symbols.  
  
## See Also  
 [IDiaLoadCallback2](../vs140/IDiaLoadCallback2.md)