---
title: "CNoWorkerThread::AddTimer"
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
ms.assetid: d9ecc65e-1d2e-4be8-8669-561fe1a5e150
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CNoWorkerThread::AddTimer
Non-functional equivalent of [CWorkerThread::AddTimer](../vs140/CWorkerThread--AddTimer.md).  
  
## Syntax  
  
```  
  
      HRESULT AddTimer(  
   DWORD /* dwInterval */,  
   IWorkerThreadClient * /* pClient */,  
   DWORD_PTR /* dwParam */,  
   HANDLE * /* phTimer */   
) throw( );  
```  
  
## Return Value  
 Always returns S_OK.  
  
## Remarks  
 The implementation provided by this class does nothing.  
  
## Requirements  
 **Header:** atlutil.h  
  
## See Also  
 [CNoWorkerThread Class](../vs140/CNoWorkerThread-Class.md)