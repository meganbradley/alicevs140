---
title: "COleControl::AmbientScaleUnits"
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
ms.assetid: e4871dd8-41f6-4727-ad69-6b60e8d24185
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::AmbientScaleUnits
Returns the type of units used by the container.  
  
## Syntax  
  
```  
  
CString AmbientScaleUnits( );  
```  
  
## Return Value  
 A string containing the ambient ScaleUnits of the container. If this property is not supported, this function returns a zero-length string.  
  
## Remarks  
 The container's ambient ScaleUnits property can be used to display positions or dimensions, labeled with the chosen unit, such as twips or centimeters. Note that the container is not required to support this property.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::TransformCoords](../vs140/COleControl--TransformCoords.md)