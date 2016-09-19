---
title: "CDockingManager::OnActivateFrame"
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
ms.assetid: 39e50cd9-6097-4921-b907-9cfc2321a561
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDockingManager::OnActivateFrame
Called by the framework when the frame window is made active or is deactivated.  
  
## Syntax  
  
```  
virtual void OnActivateFrame(  
   BOOL bActivate  
);  
```  
  
#### Parameters  
 [in] `bActivate`  
 If `TRUE`, the frame window is made active; if `FALSE`, the frame window is deactivated.  
  
## Requirements  
 **Header:** afxdockingmanager.h  
  
## See Also  
 [CDockingManager Class](../vs140/CDockingManager-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)