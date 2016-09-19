---
title: "CDockState::GetVersion"
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
ms.assetid: e3d9071b-5abd-4e0e-bcb8-aa9724f95b5c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDockState::GetVersion
Call this function to retrieve the version number of the stored bar state.  
  
## Syntax  
  
```  
  
DWORD GetVersion( );  
  
```  
  
## Return Value  
 1 if the stored bar information is older than current bar state; 2 if the stored bar information is the same as the current bar state.  
  
## Remarks  
 Version support enables a revised bar to add new persistent properties and still be able to detect and load the persistent state created by an earlier version of the bar.  
  
## Requirements  
 **Header:** afxadv.h  
  
## See Also  
 [CDockState Class](../vs140/CDockState-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDockState::LoadState](../vs140/CDockState--LoadState.md)   
 [CDockState::SaveState](../vs140/CDockState--SaveState.md)   
 [CDockState::Clear](../vs140/CDockState--Clear.md)   
 [CFrameWnd::GetDockState](../vs140/CFrameWnd--GetDockState.md)   
 [CFrameWnd::SetDockState](../vs140/CFrameWnd--SetDockState.md)