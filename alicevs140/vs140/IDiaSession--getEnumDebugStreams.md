---
title: "IDiaSession::getEnumDebugStreams"
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
ms.assetid: d294954b-80e9-476c-b9f0-5ca6fd575f68
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaSession::getEnumDebugStreams
Retrieves an enumerated sequence of debug data streams.  
  
## Syntax  
  
```cpp#  
HRESULT getEnumDebugStreams (   
   IDiaEnumDebugStreams** ppEnumDebugStreams  
)  
```  
  
#### Parameters  
 `ppEnumDebugStreams`  
 [out] Returns an [IDiaEnumDebugStreams](../vs140/IDiaEnumDebugStreams.md) object that contains a list of debug streams.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## See Also  
 [IDiaSession](../vs140/IDiaSession.md)   
 [IDiaEnumDebugStreams](../vs140/IDiaEnumDebugStreams.md)