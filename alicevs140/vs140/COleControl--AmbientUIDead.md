---
title: "COleControl::AmbientUIDead"
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
ms.assetid: 8d797864-0150-431d-824b-9da87e906c49
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::AmbientUIDead
Determines if the container wants the control to respond to user-interface actions.  
  
## Syntax  
  
```  
  
BOOL AmbientUIDead( );  
```  
  
## Return Value  
 Nonzero if the control should respond to user-interface actions; otherwise 0. If this property is not supported, this function returns 0.  
  
## Remarks  
 For example, a container might set this to **TRUE** in design mode.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::AmbientUserMode](../vs140/COleControl--AmbientUserMode.md)