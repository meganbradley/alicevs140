---
title: "CWinAppEx::ReloadWindowPlacement"
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
ms.assetid: 47199d83-d69b-46fc-a6ab-1ed2420d987b
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinAppEx::ReloadWindowPlacement
Reloads the size and location of a window from the registry.  
  
## Syntax  
  
```  
virtual BOOL ReloadWindowPlacement(  
   CFrameWnd* pFrame   
);  
```  
  
#### Parameters  
 [in] `pFrame`  
 A pointer to a frame window.  
  
## Return Value  
 Nonzero if the method was successful; 0 if the load failed or there is no data to load.  
  
## Remarks  
 Use the function [CWinAppEx::StoreWindowPlacement](../vs140/CWinAppEx--StoreWindowPlacement.md) to write the size and location of a window to the registry.  
  
## Requirements  
 **Header:** afxwinappex.h  
  
## See Also  
 [CWinAppEx Class](../vs140/CWinAppEx-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CWinAppEx::StoreWindowPlacement](../vs140/CWinAppEx--StoreWindowPlacement.md)