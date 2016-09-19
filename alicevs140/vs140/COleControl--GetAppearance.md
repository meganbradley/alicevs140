---
title: "COleControl::GetAppearance"
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
ms.assetid: f1d4c9b3-c257-4983-9527-dbfc3077f4cc
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::GetAppearance
Implements the Get function of your control's stock Appearance property.  
  
## Syntax  
  
```  
  
short GetAppearance ( );  
```  
  
## Return Value  
 The return value specifies the current appearance setting as a **short** (`VT_I2`) value, if successful. This value is zero if the control's appearance is flat and 1 if the control's appearance is 3D.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::SetAppearance](../vs140/COleControl--SetAppearance.md)   
 [COleControl::OnAppearanceChanged](../vs140/COleControl--OnAppearanceChanged.md)