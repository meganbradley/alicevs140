---
title: "CFrameWnd::GetDockState"
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
ms.assetid: 23f44f55-c7a4-4e0e-b19e-e76953eff1bc
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFrameWnd::GetDockState
Call this member function to store state information about the frame window's control bars in a `CDockState` object.  
  
## Syntax  
  
```  
  
      void GetDockState(  
   CDockState& state   
) const;  
```  
  
#### Parameters  
 `state`  
 Contains the current state of the frame window's control bars upon return.  
  
## Remarks  
 You can then write the contents of `CDockState` to storage using `CDockState::SaveState` or `Serialize`. If you later want to restore the control bars to a previous state, load the state with `CDockState::LoadState` or `Serialize`, then call `SetDockState` to apply the previous state to the frame window's control bars.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CFrameWnd Class](../vs140/CFrameWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFrameWnd::SetDockState](../vs140/CFrameWnd--SetDockState.md)   
 [CDockState Class](../vs140/CDockState-Class.md)   
 [CDockState::SaveState](../vs140/CDockState--SaveState.md)   
 [CObject::Serialize](../vs140/CObject--Serialize.md)