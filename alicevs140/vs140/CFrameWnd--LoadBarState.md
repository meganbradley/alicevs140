---
title: "CFrameWnd::LoadBarState"
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
ms.assetid: 55af47fa-0aa4-4959-bbb2-6743286d6797
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFrameWnd::LoadBarState
Call this function to restore the settings of each control bar owned by the frame window.  
  
## Syntax  
  
```  
  
      void LoadBarState(  
   LPCTSTR lpszProfileName   
);  
```  
  
#### Parameters  
 `lpszProfileName`  
 Name of a section in the initialization (INI) file or a key in the Windows registry where state information is stored.  
  
## Remarks  
 Information restored includes visibility, horizontal/vertical orientation, docking state, and control-bar position.  
  
 The settings you want to restore must be written to the registry before you call `LoadBarState`. Write the information to the registry by calling [CWinApp::SetRegistryKey](../vs140/CWinApp--SetRegistryKey.md). Write the information to the INI file by calling [SaveBarState](../vs140/CFrameWnd--SaveBarState.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CFrameWnd Class](../vs140/CFrameWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFrameWnd::SaveBarState](../vs140/CFrameWnd--SaveBarState.md)   
 [CWinApp::m_pszProfileName](../vs140/CWinApp--m_pszProfileName.md)