---
title: "CMFCMenuBar::EnableMenuShadows"
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
ms.assetid: 87011d37-170f-484d-9e88-ced34bea4d1a
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCMenuBar::EnableMenuShadows
Enables shadows for pop-up menus.  
  
## Syntax  
  
```  
static void EnableMenuShadows(  
   BOOL bEnable = TRUE  
);  
```  
  
#### Parameters  
 [in] `bEnable`  
 A Boolean parameter that indicates whether shadows should be enabled for pop-up menus.  
  
## Remarks  
 The algorithm that this method uses is complex and may decrease the performance of your application on slower systems.  
  
## Requirements  
 **Header:** afxmenubar.h  
  
## See Also  
 [CMFCMenuBar Class](../vs140/CMFCMenuBar-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)