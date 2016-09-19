---
title: "CWinAppEx::LoadWindowPlacement"
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
ms.assetid: be8075fb-2796-4769-baec-8fe64994241d
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinAppEx::LoadWindowPlacement
Called by the framework when it loads the size and location of the main frame window from the registry.  
  
## Syntax  
  
```  
virtual BOOL LoadWindowPlacement(  
   CRect& rectNormalPosition,  
   int& nFlags,  
   int& nShowCmd   
);  
```  
  
#### Parameters  
 [out] `rectNormalPosition`  
 A rectangle that contains the coordinates of the main frame window when it is in the restored position.  
  
 [out] `nFlags`  
 Flags that control the position of the minimized window and how the operating system switches between a minimized window and a restored window.  
  
 [out] `nShowCmd`  
 An integer that specifies the show state of the window. For more information about possible values, see [CWnd::ShowWindow](../vs140/CWnd--ShowWindow.md).  
  
## Return Value  
 Nonzero if successful; 0 otherwise.  
  
## Remarks  
 By default, MFC automatically loads the previous position and state of the main frame window when the application starts. For more information about how this information is stored in the registry, see [CWinAppEx::StoreWindowPlacement](../vs140/CWinAppEx--StoreWindowPlacement.md).  
  
 Override this method if you want to load additional information about the main frame window.  
  
## Requirements  
 **Header:** afxwinappex.h  
  
## See Also  
 [CWinAppEx Class](../vs140/CWinAppEx-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CWinAppEx::StoreWindowPlacement](../vs140/CWinAppEx--StoreWindowPlacement.md)