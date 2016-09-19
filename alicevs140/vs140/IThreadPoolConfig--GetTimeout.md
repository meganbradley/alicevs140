---
title: "IThreadPoolConfig::GetTimeout"
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
ms.assetid: 9a746b5c-d42a-4455-bddd-d7d497eeaa5c
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IThreadPoolConfig::GetTimeout
Call this method to get the maximum time in milliseconds that the thread pool will wait for a thread to shut down.  
  
## Syntax  
  
```  
  
      STDMETHOD(GetTimeout)(  
   DWORD * pdwMaxWait   
);  
```  
  
#### Parameters  
 `pdwMaxWait`  
 [out] Address of the variable that, on success, receives the maximum time in milliseconds that the thread pool will wait for a thread to shut down.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Example  
 See [IThreadPoolConfig::GetSize](../vs140/IThreadPoolConfig--GetSize.md).  
  
## Requirements  
 **Header:** atlutil.h  
  
## See Also  
 [IThreadPoolConfig Interface](../vs140/IThreadPoolConfig-Interface.md)   
 [IThreadPoolConfig::SetTimeout](../vs140/IThreadPoolConfig--SetTimeout.md)