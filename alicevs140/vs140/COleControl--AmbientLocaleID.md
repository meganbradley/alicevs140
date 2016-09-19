---
title: "COleControl::AmbientLocaleID"
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
ms.assetid: d8d3fc4b-1424-4d2b-be33-fb6440fa2afb
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::AmbientLocaleID
Returns the container's locale ID.  
  
## Syntax  
  
```  
  
LCID AmbientLocaleID( );  
```  
  
## Return Value  
 The value of the container's LocaleID property, if any. If this property is not supported, this function returns 0.  
  
## Remarks  
 The control can use the LocaleID to adapt its user interface for specific locales. Note that the container is not required to support this property.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)