---
title: "CFrameWnd::EndModalState"
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
ms.assetid: 7476a4b3-c8c3-4b09-980a-2b6347116f5f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFrameWnd::EndModalState
Call this member function to change a frame window from modal to modeless.  
  
## Syntax  
  
```  
  
virtual void EndModalState( );  
  
```  
  
## Remarks  
 `EndModalState` enables all of the windows disabled by [BeginModalState](../vs140/CFrameWnd--BeginModalState.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CFrameWnd Class](../vs140/CFrameWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)