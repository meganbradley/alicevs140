---
title: "CWnd::EndModalLoop"
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
ms.assetid: e49dc994-550d-4f6e-91df-9781cd3e2567
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::EndModalLoop
Terminates a call to `RunModalLoop`.  
  
## Syntax  
  
```  
  
      virtual void EndModalLoop(  
   int nResult   
);  
```  
  
#### Parameters  
 `nResult`  
 Contains the value to be returned to the caller of [RunModalLoop](../vs140/CWnd--RunModalLoop.md).  
  
## Remarks  
 The `nResult` parameter is propagated to the return value from `RunModalLoop`.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::RunModalLoop](../vs140/CWnd--RunModalLoop.md)   
 [CWnd::ContinueModal](../vs140/CWnd--ContinueModal.md)