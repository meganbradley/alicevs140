---
title: "CDockState::Clear"
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
ms.assetid: b8d7d510-0d65-45a1-afa0-acbbcd9e59c6
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDockState::Clear
Call this function to clear all docking information stored in the `CDockState` object.  
  
## Syntax  
  
```  
  
void Clear( );  
  
```  
  
## Remarks  
 This includes not only whether the bar is docked or not, but the bar's size and position and whether or not it is visible.  
  
## Requirements  
 **Header:** afxadv.h  
  
## See Also  
 [CDockState Class](../vs140/CDockState-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDockState::LoadState](../vs140/CDockState--LoadState.md)   
 [CDockState::SaveState](../vs140/CDockState--SaveState.md)   
 [CDockState::GetVersion](../vs140/CDockState--GetVersion.md)   
 [CFrameWnd::GetDockState](../vs140/CFrameWnd--GetDockState.md)   
 [CFrameWnd::SetDockState](../vs140/CFrameWnd--SetDockState.md)