---
title: "CWinApp::LoadStdProfileSettings"
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
ms.assetid: c23205b4-580b-431d-9c68-3710e6aaa29a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinApp::LoadStdProfileSettings
Call this member function from within the [InitInstance](../vs140/CWinApp--InitInstance.md) member function to enable and load the list of most recently used (MRU) files and last preview state.  
  
## Syntax  
  
```  
  
      void LoadStdProfileSettings(  
   UINT nMaxMRU = _AFX_MRU_COUNT   
);  
```  
  
#### Parameters  
 `nMaxMRU`  
 The number of recently used files to track.  
  
## Remarks  
 If `nMaxMRU` is 0, no MRU list will be maintained.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWinApp Class](../vs140/CWinApp-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWinApp::OnFileOpen](../vs140/CWinApp--OnFileOpen.md)   
 [CWinApp::AddToRecentFileList](../vs140/CWinApp--AddToRecentFileList.md)