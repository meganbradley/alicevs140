---
title: "CWinAppEx::StoreWindowPlacement"
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
ms.assetid: a3db2f75-cc73-4bd6-bb25-0596e83e86b2
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinAppEx::StoreWindowPlacement
Called by the framework to write the size and location of the main frame window to the registry.  
  
## Syntax  
  
```  
virtual BOOL StoreWindowPlacement(  
   const CRect& rectNormalPosition,  
   int nFlags,  
   int nShowCmd   
);  
```  
  
#### Parameters  
 [in] `nFlags`  
 Flags that control the position of the minimized window and how the operating system switches between a minimized window and a restored window.  
  
 [in] `nShowCmd`  
 An integer that specifies the show state of the window. For more information about possible values, see [CWnd::ShowWindow](../vs140/CWnd--ShowWindow.md).  
  
 [in] `rectNormalPosition`  
 A rectangle that contains the coordinates of the main frame window when it is in the restored state.  
  
## Return Value  
 Nonzero if successful; 0 otherwise.  
  
## Remarks  
 By default, MFC automatically saves the position and state of the main frame window before the application exits. This information is stored in the Windows registry under the WindowPlacement key in the default registry location for your application. For more information about the default registry location of your application, see [CWinAppEx::GetRegistryBase](../vs140/CWinAppEx--GetRegistryBase.md).  
  
 Override this method if you want to store additional information about the main frame window.  
  
## Requirements  
 **Header:** afxwinappex.h  
  
## See Also  
 [CWinAppEx Class](../vs140/CWinAppEx-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CWinAppEx::LoadWindowPlacement](../vs140/CWinAppEx--LoadWindowPlacement.md)