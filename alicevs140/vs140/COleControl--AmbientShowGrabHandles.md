---
title: "COleControl::AmbientShowGrabHandles"
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
ms.assetid: 829d92c2-5f3f-440c-9a9b-9a72af967e5d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::AmbientShowGrabHandles
Determines whether the container allows the control to display grab handles for itself when active.  
  
## Syntax  
  
```  
  
BOOL AmbientShowGrabHandles( );  
```  
  
## Return Value  
 Nonzero if grab handles should be displayed; otherwise 0. If this property is not supported, this function returns nonzero.  
  
## Remarks  
 Note that the container is not required to support this property.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::AmbientShowHatching](../vs140/COleControl--AmbientShowHatching.md)