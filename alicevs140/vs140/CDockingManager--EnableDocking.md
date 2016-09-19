---
title: "CDockingManager::EnableDocking"
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
ms.assetid: 651d7f24-a3f2-4d2e-94a1-6da9829249d5
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDockingManager::EnableDocking
Creates a dock pane and enables docking of the pane to the main frame.  
  
## Syntax  
  
```  
BOOL EnableDocking(  
   DWORD dwStyle  
);  
```  
  
#### Parameters  
 [in] `dwStyle`  
 The docking alignment.  
  
## Return Value  
 `TRUE` if the dock pane was created successfully; `FALSE` otherwise.  
  
## Requirements  
 **Header:** afxdockingmanager.h  
  
## See Also  
 [CDockingManager Class](../vs140/CDockingManager-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)