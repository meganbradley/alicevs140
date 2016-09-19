---
title: "IDiaEnumInjectedSources::Item"
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
ms.assetid: 14846955-7270-451d-91d2-9cb34bb65187
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaEnumInjectedSources::Item
Retrieves an injected source by means of an index.  
  
## Syntax  
  
```cpp#  
HRESULT Item (   
   DWORD                index,  
   IDiaInjectedSource** injectedSource  
);  
```  
  
#### Parameters  
 index  
 [in] Index of the [IDiaInjectedSource](../vs140/IDiaInjectedSource.md) object to be retrieved. The index is the range 0 to `count`-1, where `count` is returned by the [IDiaEnumInjectedSources::get_Count](../vs140/IDiaEnumInjectedSources--get_Count.md) method.  
  
 injectedSource  
 [out] Returns an [IDiaInjectedSource](../vs140/IDiaInjectedSource.md) object representing the injected source.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## See Also  
 [IDiaEnumInjectedSources](../vs140/IDiaEnumInjectedSources.md)   
 [IDiaInjectedSource](../vs140/IDiaInjectedSource.md)