---
title: "CBasePane::AdjustDockingLayout"
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
ms.assetid: fa6561fb-69aa-4825-8c27-c3de729135e5
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBasePane::AdjustDockingLayout
Redirects a call to the docking manager to adjust the docking layout.  
  
## Syntax  
  
```  
virtual void AdjustDockingLayout(  
   HDWP hdwp=NULL   
);  
```  
  
#### Parameters  
 [out] `hdwp`  
 A handle to a structure containing multiple window positions.  
  
## Remarks  
 This is a convenience method that adjusts the docking layout. By using this method, you do not have to write code that analyzes the type of the parent frame.  
  
 For more information, see [CDockingManager::AdjustDockingLayout](../vs140/CDockingManager--AdjustDockingLayout.md)  
  
## Requirements  
 **Header:** afxbasepane.h  
  
## See Also  
 [CBasePane Class](../vs140/CBasePane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)