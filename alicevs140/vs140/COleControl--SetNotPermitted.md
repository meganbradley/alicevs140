---
title: "COleControl::SetNotPermitted"
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
ms.assetid: eb440f17-cee6-4f72-ab3f-edfb9a685075
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::SetNotPermitted
Indicates that an edit request has failed.  
  
## Syntax  
  
```  
  
void SetNotPermitted( );  
```  
  
## Remarks  
 Call this function when `BoundPropertyRequestEdit` fails. This function throws an exception of type **COleDispScodeException** to indicate that the set operation was not permitted.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::BoundPropertyRequestEdit](../vs140/COleControl--BoundPropertyRequestEdit.md)