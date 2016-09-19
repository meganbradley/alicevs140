---
title: "COleControl::GetNotSupported"
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
ms.assetid: c2dbc2d3-8f1c-4b12-b014-4262486af586
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::GetNotSupported
Prevents access to a control's property value by the user.  
  
## Syntax  
  
```  
  
void GetNotSupported( );  
```  
  
## Remarks  
 Call this function in place of the Get function of any property where retrieval of the property by the control's user is not supported. One example would be a property that is write only.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::SetNotSupported](../vs140/COleControl--SetNotSupported.md)