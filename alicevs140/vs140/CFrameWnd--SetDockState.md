---
title: "CFrameWnd::SetDockState"
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
ms.assetid: af599457-1eb6-4337-86d3-771bd71a4cc3
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFrameWnd::SetDockState
Call this member function to apply state information stored in a `CDockState` object to the frame window's control bars.  
  
## Syntax  
  
```  
  
      void SetDockState(  
   const CDockState& state   
);  
```  
  
#### Parameters  
 `state`  
 Apply the stored state to the frame window's control bars.  
  
## Remarks  
 To restore a previous state of the control bars, you can load the stored state with `CDockState::LoadState` or `Serialize`, then use `SetDockState` to apply it to the frame window's control bars. The previous state is stored in the `CDockState` object with `GetDockState`  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CFrameWnd Class](../vs140/CFrameWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFrameWnd::GetDockState](../vs140/CFrameWnd--GetDockState.md)   
 [CDockState Class](../vs140/CDockState-Class.md)   
 [CDockState::LoadState](../vs140/CDockState--LoadState.md)   
 [CObject::Serialize](../vs140/CObject--Serialize.md)