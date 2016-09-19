---
title: "COleControl::AmbientShowHatching"
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
ms.assetid: 077fcbc4-5979-4bf9-8cbe-5059c8ae0791
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::AmbientShowHatching
Determines whether the container allows the control to display itself with a hatched pattern when UI active.  
  
## Syntax  
  
```  
  
BOOL AmbientShowHatching( );  
```  
  
## Return Value  
 Nonzero if the hatched pattern should be shown; otherwise 0. If this property is not supported, this function returns nonzero.  
  
## Remarks  
 Note that the container is not required to support this property.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::AmbientShowGrabHandles](../vs140/COleControl--AmbientShowGrabHandles.md)