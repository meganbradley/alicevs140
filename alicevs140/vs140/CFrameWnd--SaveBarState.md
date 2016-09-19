---
title: "CFrameWnd::SaveBarState"
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
ms.assetid: 3b4e7f29-935f-4693-8d6c-9de2e86f5295
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFrameWnd::SaveBarState
Call this function to store information about each control bar owned by the frame window.  
  
## Syntax  
  
```  
  
      void SaveBarState(  
   LPCTSTR lpszProfileName   
) const;  
```  
  
#### Parameters  
 `lpszProfileName`  
 Name of a section in the initialization file or a key in the Windows registry where state information is stored.  
  
## Remarks  
 This information can be read from the initialization file using [LoadBarState](../vs140/CFrameWnd--LoadBarState.md). Information stored includes visibility, horizontal/vertical orientation, docking state, and control bar position.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CFrameWnd Class](../vs140/CFrameWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFrameWnd::LoadBarState](../vs140/CFrameWnd--LoadBarState.md)   
 [CWinApp::SetRegistryKey](../vs140/CWinApp--SetRegistryKey.md)   
 [CWinApp::m_pszProfileName](../vs140/CWinApp--m_pszProfileName.md)