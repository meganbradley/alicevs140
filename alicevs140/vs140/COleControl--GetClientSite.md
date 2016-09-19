---
title: "COleControl::GetClientSite"
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
ms.assetid: b1e1ed2b-b778-4fae-a899-93214d57b0ac
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::GetClientSite
Queries an object for the pointer to its current client site within its container.  
  
## Syntax  
  
```  
  
LPOLECLIENTSITE GetClientSite( );  
```  
  
## Return Value  
 A pointer to the control's current client site in its container.  
  
## Remarks  
 The returned pointer points to an instance of `IOleClientSite`. The `IOleClientSite` interface, implemented by containers, is the object's view of its context: where it is anchored in the document, where it gets its storage, user interface, and other resources.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)