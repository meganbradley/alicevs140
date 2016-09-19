---
title: "CAtlDllModuleT::DllCanUnloadNow"
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
ms.assetid: 7cd8a62b-d4d2-4435-8d94-5f8b4305ab77
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlDllModuleT::DllCanUnloadNow
Tests if the DLL can be unloaded.  
  
## Syntax  
  
```  
  
HRESULT DllCanUnloadNow( ) throw( );  
  
```  
  
## Return Value  
 Returns S_OK if the DLL can be unloaded, or S_FALSE if it cannot.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CAtlDllModuleT Class](../vs140/CAtlDllModuleT-Class.md)