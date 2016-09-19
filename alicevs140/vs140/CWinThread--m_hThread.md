---
title: "CWinThread::m_hThread"
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
ms.assetid: fe288030-72ea-4839-bea5-6575865c3533
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinThread::m_hThread
Handle to the thread attached to this `CWinThread`.  
  
## Syntax  
  
```  
  
HANDLE m_hThread;  
  
```  
  
## Remarks  
 The `m_hThread` data member is a public variable of type `HANDLE`. It is only valid if underlying thread currently exists.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinThread Class](../vs140/CWinThread-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)