---
title: "CDockablePaneAdapter::LoadState"
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
ms.assetid: 377c0c04-33cd-40c7-b7c5-b14b625d4f11
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDockablePaneAdapter::LoadState
Loads the state of the pane from the registry.  
  
## Syntax  
  
```  
virtual BOOL LoadState(  
   LPCTSTR lpszProfileName = NULL,  
   int nIndex = -1,  
   UINT uiID = (UINT) -1  
);  
```  
  
#### Parameters  
 [in] `lpszProfileName`  
 The profile name.  
  
 [in] `nIndex`  
 The profile index.  
  
 [in] `uiID`  
 The pane ID.  
  
## Return Value  
  
## Remarks  
  
## Requirements  
 **Header:** afxdockablepaneadapter.h  
  
## See Also  
 [CDockablePaneAdapter Class](../vs140/CDockablePaneAdapter-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)