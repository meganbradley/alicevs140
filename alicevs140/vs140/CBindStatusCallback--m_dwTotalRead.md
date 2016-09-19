---
title: "CBindStatusCallback::m_dwTotalRead"
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
ms.assetid: 105e2250-5c03-4719-b48e-defef0cbb31f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBindStatusCallback::m_dwTotalRead
The cumulative total of bytes read in the asynchronous data transfer.  
  
## Syntax  
  
```  
  
DWORD m_dwTotalRead;  
  
```  
  
## Remarks  
 Incremented every time `OnDataAvailable` is called by the number of bytes actually read. Initialized to zero in `StartAsyncDownload`.  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [CBindStatusCallback Class](../vs140/CBindStatusCallback-Class.md)   
 [CBindStatusCallback::StartAsyncDownload](../vs140/CBindStatusCallback--StartAsyncDownload.md)   
 [CBindStatusCallback::OnDataAvailable](../vs140/CBindStatusCallback--OnDataAvailable.md)