---
title: "CThreadPool::QueryInterface"
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
ms.assetid: 962b28f8-24fd-4a43-b5ac-df0d8c2dd858
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CThreadPool::QueryInterface
Implementation of **IUnknown::QueryInterface**.  
  
## Syntax  
  
```  
  
      HRESULT STDMETHODCALLTYPE QueryInterface(  
   REFIID riid,  
   void** ppv   
) throw( );  
```  
  
## Remarks  
 Objects of this class can be successfully queried for the **IUnknown** and [IThreadPoolConfig](../vs140/IThreadPoolConfig-Interface.md) interfaces.  
  
## Requirements  
 **Header:** atlutil.h  
  
## See Also  
 [CThreadPool Class](../vs140/CThreadPool-Class.md)