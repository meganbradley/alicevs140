---
title: "CWinAppEx::EnableLoadWindowPlacement"
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
ms.assetid: 3753b04e-8270-4a64-999b-578f62a2d191
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinAppEx::EnableLoadWindowPlacement
Specifies whether the application will load the initial size and location of the main frame window from the registry.  
  
## Syntax  
  
```  
void EnableLoadWindowPlacement(  
   BOOL bEnable = TRUE  
);  
```  
  
#### Parameters  
 [in] `bEnable`  
 Specifies whether the application loads the initial size and location of the main frame window from the registry.  
  
## Remarks  
 By default, the size and location of the main frame is loaded from the registry together with other application settings. This occurs during [CWinAppEx::LoadState](../vs140/CWinAppEx--LoadState.md). If you do not want to load the initial window placement from the registry, call this method with `bEnable` set to `false`.  
  
## Requirements  
 **Header:** afxwinappex.h  
  
## See Also  
 [CWinAppEx Class](../vs140/CWinAppEx-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)