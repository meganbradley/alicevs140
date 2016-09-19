---
title: "CDockingManager::Create"
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
ms.assetid: 491f54d8-2b2c-4f3c-8433-78471112c536
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDockingManager::Create
Creates a docking manager.  
  
## Syntax  
  
```  
BOOL Create(  
   CFrameWnd* pParentWnd  
);  
```  
  
#### Parameters  
 [in] `pParentWnd`  
 A pointer to the parent frame of the docking manager. This value must not be `NULL`.  
  
## Return Value  
 `TRUE` always.  
  
## Requirements  
 **Header:** afxdockingmanager.h  
  
## See Also  
 [CDockingManager Class](../vs140/CDockingManager-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)