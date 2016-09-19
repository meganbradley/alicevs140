---
title: "CMFCMenuBar::SaveState"
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
ms.assetid: b0588241-9df7-4aa6-86cf-789b06455500
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCMenuBar::SaveState
Saves the state of the [CMFCMenuBar](../vs140/CMFCMenuBar-Class.md) object to the Windows registry.  
  
## Syntax  
  
```  
virtual BOOL SaveState (  
   LPCTSTR lpszProfileName = NULL,  
   int nIndex = -1,  
   UINT uiID = (UINT)-1  
);  
```  
  
#### Parameters  
 [in] `lpszProfileName`  
 A string that contains the path of a Windows registry key.  
  
 [in] `nIndex`  
 The control ID for the menu bar.  
  
 [in] `uiID`  
 A reserved value.  
  
## Return Value  
 `TRUE` if successful; otherwise `FALSE`;  
  
## Remarks  
 Usually, your application does not call `SaveState`. The framework calls this method when the workspace is serialized. For more information, see [CWinAppEx::SaveState](../vs140/CWinAppEx--SaveState.md).  
  
 The saved information includes the menu items, the dock state, and the position of the menu bar.  
  
## Requirements  
 **Header:** afxmenubar.h  
  
## See Also  
 [CMFCMenuBar Class](../vs140/CMFCMenuBar-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCMenuBar::LoadState](../vs140/CMFCMenuBar--LoadState.md)