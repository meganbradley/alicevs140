---
title: "CWnd::ContinueModal"
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
ms.assetid: 2c215d85-c068-4eb8-b58f-1090b2e8b271
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::ContinueModal
This member function is called by [RunModalLoop](../vs140/CWnd--RunModalLoop.md) to determine when the modal state should be exited.  
  
## Syntax  
  
```  
  
virtual BOOL ContinueModal( );  
  
```  
  
## Return Value  
 Nonzero if modal loop is to be continued; 0 when [EndModalLoop](../vs140/CWnd--EndModalLoop.md) is called.  
  
## Remarks  
 By default, it returns non-zero until `EndModalLoop` is called.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::RunModalLoop](../vs140/CWnd--RunModalLoop.md)   
 [CWnd::EndModalLoop](../vs140/CWnd--EndModalLoop.md)