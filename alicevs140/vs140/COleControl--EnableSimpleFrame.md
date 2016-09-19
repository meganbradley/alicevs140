---
title: "COleControl::EnableSimpleFrame"
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
ms.assetid: 23bd09b5-28a1-44bf-a9d3-2a9c79b5fd09
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::EnableSimpleFrame
Enables the simple frame characteristic for an OLE control.  
  
## Syntax  
  
```  
  
void EnableSimpleFrame( );  
```  
  
## Remarks  
 This characteristic allows a control to support visual containment of other controls, but not true OLE containment. An example would be a group box with several controls inside. These controls are not OLE contained, but they are in the same group box.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)