---
title: "IDiaSession::findInjectedSource"
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
ms.assetid: 907531b6-1ef8-4153-986d-b72611a1632d
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaSession::findInjectedSource
Retrieves a list of sources that has been placed into the symbol store by attribute providers or other components of the compilation process.  
  
## Syntax  
  
```cpp#  
HRESULT findInjectedSource (   
   LPCOLESTR                 srcFile,  
   IDiaEnumInjectedSources** ppResult  
);  
```  
  
#### Parameters  
 srcFile  
 [in] Name of the source file for which to search.  
  
 ppResult  
 [out] Returns an [IDiaEnumInjectedSources](../vs140/IDiaEnumInjectedSources.md) object that contains a list of all of the injected sources.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## See Also  
 [IDiaEnumInjectedSources](../vs140/IDiaEnumInjectedSources.md)   
 [IDiaSession](../vs140/IDiaSession.md)