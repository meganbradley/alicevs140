---
title: "IThreadPoolConfig::SetTimeout"
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
ms.assetid: b82a1dc3-0c16-4bb8-bb7b-b4055bf719c5
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IThreadPoolConfig::SetTimeout
Call this method to set the maximum time in milliseconds that the thread pool will wait for a thread to shut down.  
  
## Syntax  
  
```  
  
      STDMETHOD(SetTimeout)(  
   DWORD dwMaxWait   
);  
```  
  
#### Parameters  
 `dwMaxWait`  
 The requested maximum time in milliseconds that the thread pool will wait for a thread to shut down.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Example  
 See [IThreadPoolConfig::GetSize](../vs140/IThreadPoolConfig--GetSize.md).  
  
## Requirements  
 **Header:** atlutil.h  
  
## See Also  
 [IThreadPoolConfig Interface](../vs140/IThreadPoolConfig-Interface.md)   
 [IThreadPoolConfig::GetTimeout](../vs140/IThreadPoolConfig--GetTimeout.md)