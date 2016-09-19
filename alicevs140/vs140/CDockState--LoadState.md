---
title: "CDockState::LoadState"
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
ms.assetid: dd3448c4-4104-4847-ba96-7a44d0cd9994
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDockState::LoadState
Call this function to retrieve state information from the registry or .INI file.  
  
## Syntax  
  
```  
  
      void LoadState(  
   LPCTSTR lpszProfileName   
);  
```  
  
#### Parameters  
 `lpszProfileName`  
 Points to a null-teminated string that specifies the name of a section in the initialization file or a key in the Windows registry where state information is stored.  
  
## Remarks  
 The profile name is the section of the application's .INI file or the registry that contains the bars' state information. You can save control bar state information to the registry or .INI file with `SaveState`.  
  
## Requirements  
 **Header:** afxadv.h  
  
## See Also  
 [CDockState Class](../vs140/CDockState-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDockState::SaveState](../vs140/CDockState--SaveState.md)   
 [CDockState::GetVersion](../vs140/CDockState--GetVersion.md)   
 [CDockState::Clear](../vs140/CDockState--Clear.md)   
 [CFrameWnd::GetDockState](../vs140/CFrameWnd--GetDockState.md)   
 [CFrameWnd::SetDockState](../vs140/CFrameWnd--SetDockState.md)