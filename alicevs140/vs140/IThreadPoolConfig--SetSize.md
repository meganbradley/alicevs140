---
title: "IThreadPoolConfig::SetSize"
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
ms.assetid: 76cd3f79-d59b-4b7f-876b-6d431eae5ea8
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IThreadPoolConfig::SetSize
Call this method to set the number of threads in the pool.  
  
## Syntax  
  
```  
  
      STDMETHOD(SetSize)(  
   int nNumThreads   
);  
```  
  
#### Parameters  
 `nNumThreads`  
 The requested number of threads in the pool.  
  
 If `nNumThreads` is negative, its absolute value will be multiplied by the number of processors in the machine to get the total number of threads.  
  
 If `nNumThreads` is zero, [ATLS_DEFAULT_THREADSPERPROC](../vs140/ATLS_DEFAULT_THREADSPERPROC.md) will be multiplied by the number of processors in the machine to get the total number of threads.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Example  
 See [IThreadPoolConfig::GetSize](../vs140/IThreadPoolConfig--GetSize.md).  
  
## Requirements  
 **Header:** atlutil.h  
  
## See Also  
 [IThreadPoolConfig Interface](../vs140/IThreadPoolConfig-Interface.md)   
 [IThreadPoolConfig::GetSize](../vs140/IThreadPoolConfig--GetSize.md)