---
title: "CNoWorkerThread::AddHandle"
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
ms.assetid: bf35bc89-e448-4cf0-b027-75223763d482
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CNoWorkerThread::AddHandle
Non-functional equivalent of [CWorkerThread::AddHandle](../vs140/CWorkerThread--AddHandle.md).  
  
## Syntax  
  
```  
  
      HRESULT AddHandle(  
   HANDLE /* hObject */,  
   IWorkerThreadClient * /* pClient */,  
   DWORD_PTR /* dwParam */   
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