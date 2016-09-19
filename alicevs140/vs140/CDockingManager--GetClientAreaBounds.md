---
title: "CDockingManager::GetClientAreaBounds"
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
ms.assetid: c9f83c2b-ec9a-4bec-926d-dcce7b99adbb
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDockingManager::GetClientAreaBounds
Gets the rectangle that contains the bounds of the client area.  
  
## Syntax  
  
```  
CRect GetClientAreaBounds() const;  
void GetClientAreaBounds(  
   CRect & rcClient  
);  
```  
  
#### Parameters  
 [out] `rcClient`  
 A reference to the rectangle that contains the bounds of the client area.  
  
## Return Value  
 The rectangle that contains the bounds of the client area.  
  
## Requirements  
 **Header:** afxdockingmanager.h  
  
## See Also  
 [CDockingManager Class](../vs140/CDockingManager-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)