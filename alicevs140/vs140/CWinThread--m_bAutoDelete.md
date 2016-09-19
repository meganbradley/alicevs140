---
title: "CWinThread::m_bAutoDelete"
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
ms.assetid: c4cd5f2a-31f9-45fe-8bfe-ef5af16d699c
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinThread::m_bAutoDelete
Specifies whether the `CWinThread` object should be automatically deleted at thread termination.  
  
## Syntax  
  
```  
  
BOOL m_bAutoDelete;  
  
```  
  
## Remarks  
 The `m_bAutoDelete` data member is a public variable of type **BOOL**.  
  
 The value of `m_bAutoDelete` does not affect how the underlying thread handle is closed. The thread handle is always closed when the `CWinThread` object is destroyed.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinThread Class](../vs140/CWinThread-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [AfxBeginThread](../vs140/AfxBeginThread.md)   
 [CWinThread::ResumeThread](../vs140/CWinThread--ResumeThread.md)