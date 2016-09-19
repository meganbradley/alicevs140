---
title: "CMFCMenuBar::LoadState"
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
ms.assetid: fca3d59c-2f52-4068-8fb8-607bbe233e9e
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCMenuBar::LoadState
Loads the state of the menu bar from the Windows registry.  
  
## Syntax  
  
```  
virtual BOOL LoadState(  
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
 `TRUE` if the method was successful; otherwise `FALSE`.  
  
## Remarks  
 Use the [CMFCMenuBar::SaveState](../vs140/CMFCMenuBar--SaveState.md) method to save the state of the menu bar to the registry. The saved information includes the menu items, the dock state, and the position of the menu bar.  
  
 In most cases your application does not call `LoadState`. The framework calls this method when it initializes the workspace.  
  
## Requirements  
 **Header:** afxmenubar.h  
  
## See Also  
 [CMFCMenuBar Class](../vs140/CMFCMenuBar-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCMenuBar::SaveState](../vs140/CMFCMenuBar--SaveState.md)