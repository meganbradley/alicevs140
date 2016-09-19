---
title: "IDiaEnumInjectedSources::Next"
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
ms.assetid: 38af80fc-748f-4b15-bff1-823db21dd4d0
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaEnumInjectedSources::Next
Retrieves a specified number of injected sources in the enumeration sequence.  
  
## Syntax  
  
```cpp#  
HRESULT Next (   
   ULONG                celt,   
   IDiaInjectedSource** rgelt,  
   ULONG*               pceltFetched  
);  
```  
  
#### Parameters  
 celt  
 [in] The number of injected sources in the enumerator to be retrieved.  
  
 rgelt  
 [out] Returns an array of [IDiaInjectedSource](../vs140/IDiaInjectedSource.md) objects that represents the desired injected sources.  
  
 pceltFetched  
 [out] Returns the number of injected sources in the fetched enumerator.  
  
## Return Value  
 If successful, returns `S_OK`. Returns `S_FALSE` if there are no more injected sources. Otherwise, returns an error code.  
  
## See Also  
 [IDiaEnumInjectedSources](../vs140/IDiaEnumInjectedSources.md)   
 [IDiaInjectedSource](../vs140/IDiaInjectedSource.md)