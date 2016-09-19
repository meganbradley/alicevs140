---
title: "COleControl::AmbientForeColor"
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
ms.assetid: 10eab1bd-220c-44b0-8e81-3a8efedd1865
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::AmbientForeColor
Returns the value of the ambient ForeColor property.  
  
## Syntax  
  
```  
  
OLE_COLOR AmbientForeColor( );  
```  
  
## Return Value  
 The current value of the container's ambient ForeColor property, if any. If not supported, this function returns the system-defined Windows text color.  
  
## Remarks  
 The ambient ForeColor property is available to all controls and is defined by the container. Note that the container is not required to support this property.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::AmbientBackColor](../vs140/COleControl--AmbientBackColor.md)   
 [COleControl::GetForeColor](../vs140/COleControl--GetForeColor.md)   
 [COleControl::TranslateColor](../vs140/COleControl--TranslateColor.md)