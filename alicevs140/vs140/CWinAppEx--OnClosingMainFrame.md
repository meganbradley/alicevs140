---
title: "CWinAppEx::OnClosingMainFrame"
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
ms.assetid: 192bb480-89f8-4ee7-a2ea-7043e1904305
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinAppEx::OnClosingMainFrame
The framework calls this method when a frame window is processing `WM_CLOSE`.  
  
## Syntax  
  
```  
virtual void OnClosingMainFrame(  
   CFrameImpl* pFrameImpl   
);  
```  
  
#### Parameters  
 [in] `pFrameImpl`  
 A pointer to a `CFrameImpl` object.  
  
## Remarks  
 The default implementation of this method saves the state of `pFrameImpl`.  
  
## Requirements  
 **Header:** afxwinappex.h  
  
## See Also  
 [CWinAppEx Class](../vs140/CWinAppEx-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)