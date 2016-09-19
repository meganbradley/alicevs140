---
title: "CDockingManager::OnMoveMiniFrame"
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
ms.assetid: 977c3537-0faf-429f-aa96-9194959ddde7
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDockingManager::OnMoveMiniFrame
Called by the framework to move a mini-frame window.  
  
## Syntax  
  
```  
virtual BOOL OnMoveMiniFrame(  
   CWnd* pFrame  
);  
```  
  
#### Parameters  
 [in] `pFrame`  
 A pointer to a mini-frame window.  
  
## Return Value  
 `TRUE` if the method succeeds; otherwise `FALSE`.  
  
## Requirements  
 **Header:** afxdockingmanager.h  
  
## See Also  
 [CDockingManager Class](../vs140/CDockingManager-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)