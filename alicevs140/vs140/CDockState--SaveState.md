---
title: "CDockState::SaveState"
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
ms.assetid: 1b6bc9af-bbd6-4dbe-a2e8-99e743f51d3d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDockState::SaveState
Call this function to save the state information to the registry or .INI file.  
  
## Syntax  
  
```  
  
      void SaveState(  
   LPCTSTR lpszProfileName   
);  
```  
  
#### Parameters  
 `lpszProfileName`  
 Points to a null-teminated string that specifies the name of a section in the initialization file or a key in the Windows registry where state information is stored.  
  
## Remarks  
 The profile name is the section of the application's .INI file or the registry that contains the control bar's state information. `SaveState` also saves the current screen size. You can retrieve control bar information from the registry or .INI file with `LoadState`.  
  
## Requirements  
 **Header:** afxadv.h  
  
## See Also  
 [CDockState Class](../vs140/CDockState-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDockState::LoadState](../vs140/CDockState--LoadState.md)   
 [CDockState::GetVersion](../vs140/CDockState--GetVersion.md)   
 [CDockState::Clear](../vs140/CDockState--Clear.md)   
 [CFrameWnd::GetDockState](../vs140/CFrameWnd--GetDockState.md)   
 [CFrameWnd::SetDockState](../vs140/CFrameWnd--SetDockState.md)