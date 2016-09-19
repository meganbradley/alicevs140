---
title: "COleControl::AmbientBackColor"
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
ms.assetid: 7fef2ec0-4697-406a-8451-5d31ef7c160b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::AmbientBackColor
Returns the value of the ambient BackColor property.  
  
## Syntax  
  
```  
  
OLE_COLOR AmbientBackColor( );  
```  
  
## Return Value  
 The current value of the container's ambient BackColor property, if any. If the property is not supported, this function returns the system-defined Windows background color.  
  
## Remarks  
 The ambient BackColor property is available to all controls and is defined by the container. Note that the container is not required to support this property.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::TranslateColor](../vs140/COleControl--TranslateColor.md)   
 [COleControl::GetBackColor](../vs140/COleControl--GetBackColor.md)   
 [COleControl::AmbientForeColor](../vs140/COleControl--AmbientForeColor.md)