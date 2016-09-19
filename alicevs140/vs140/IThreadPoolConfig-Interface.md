---
title: "IThreadPoolConfig Interface"
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
ms.assetid: 69e642bf-6925-46e6-9a37-cce52231b1cc
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IThreadPoolConfig Interface
This interface provides methods for configuring a thread pool.  
  
> [!IMPORTANT]
>  This class and its members cannot be used in applications that execute in the [!INCLUDE[wrt](../vs140/includes/wrt_md.md)].  
  
## Syntax  
  
```  
  
      __interface  
__declspec(uuid("B1F64757-6E88-4fa2-8886-7848B0D7E660"))  
IThreadPoolConfig :  
public IUnknown  
```  
  
## Members  
  
### Methods  
  
|||  
|-|-|  
|[GetSize](../vs140/IThreadPoolConfig--GetSize.md)|Call this method to get the number of threads in the pool.|  
|[GetTimeout](../vs140/IThreadPoolConfig--GetTimeout.md)|Call this method to get the maximum time in milliseconds that the thread pool will wait for a thread to shut down.|  
|[SetSize](../vs140/IThreadPoolConfig--SetSize.md)|Call this method to set the number of threads in the pool.|  
|[SetTimeout](../vs140/IThreadPoolConfig--SetTimeout.md)|Call this method to set the maximum time in milliseconds that the thread pool will wait for a thread to shut down.|  
  
## Remarks  
 This interface is implemented by [CThreadPool](../vs140/CThreadPool-Class.md).  
  
## Requirements  
 **Header:** atlutil.h  
  
## See Also  
 [ATL Classes](../vs140/ATL-Classes.md)   
 [CThreadPool Class](../vs140/CThreadPool-Class.md)