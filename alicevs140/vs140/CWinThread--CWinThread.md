---
title: "CWinThread::CWinThread"
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
ms.assetid: b7cc4951-978f-4bb0-af2a-dd5cb93d7989
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinThread::CWinThread
Constructs a `CWinThread` object.  
  
## Syntax  
  
```  
  
CWinThread( );  
```  
  
## Remarks  
 To begin the thread's execution, call the [CreateThread](../vs140/CWinThread--CreateThread.md) member function. You will usually create threads by calling [AfxBeginThread](../vs140/AfxBeginThread.md), which will call this constructor and `CreateThread`.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinThread Class](../vs140/CWinThread-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWinThread::CreateThread](../vs140/CWinThread--CreateThread.md)