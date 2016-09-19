---
title: "CWinThread::m_nThreadID"
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
ms.assetid: 20bfe043-48ac-4156-80b2-deea74e82dbc
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinThread::m_nThreadID
ID of the thread attached to this `CWinThread`.  
  
## Syntax  
  
```  
DWORD m_nThreadID;  
```  
  
## Remarks  
 The **m_nThreadID** data member is a public variable of type `DWORD`. It is only valid if underlying thread currently exists.  
  
## Example  
 See the example for [AfxGetThread](../vs140/AfxGetThread.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinThread Class](../vs140/CWinThread-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)