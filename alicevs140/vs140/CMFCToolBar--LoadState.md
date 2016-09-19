---
title: "CMFCToolBar::LoadState"
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
ms.assetid: 42480587-13fe-4a48-9ca1-4ec4d219046e
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::LoadState
Loads the toolbar state information from the Windows registry.  
  
## Syntax  
  
```  
virtual BOOL LoadState(  
   LPCTSTR lpszProfileName=NULL,  
   int nIndex=-1,  
   UINT uiID=(UINT)-1   
);  
```  
  
#### Parameters  
 [in] `lpszProfileName`  
 Specifies the relative path of the Windows registry key.  
  
 [in] `nIndex`  
 Specifies the control ID of the toolbar.  
  
 [in] `uiID`  
 Specifies the resource ID of the toolbar.  
  
## Return Value  
 Nonzero if the method succeeds; otherwise 0.  
  
## Remarks  
 The framework calls this method as a part of the initialization process of the application. For more information, see [CWinAppEx::LoadState](../vs140/CWinAppEx--LoadState.md).  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWinAppEx::LoadState](../vs140/CWinAppEx--LoadState.md)