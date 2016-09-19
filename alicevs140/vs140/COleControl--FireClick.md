---
title: "COleControl::FireClick"
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
ms.assetid: 9f9e490d-eb6e-49c9-8ca7-b2f9a166a2ed
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::FireClick
Called by the framework when the mouse is clicked over an active control.  
  
## Syntax  
  
```  
  
void FireClick( );  
```  
  
## Remarks  
 If this event is defined as a custom event, you determine when the event is fired.  
  
 For automatic firing of a Click event to occur, the control's Event map must have a stock Click event defined.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::FireDblClick](../vs140/COleControl--FireDblClick.md)   
 [COleControl::FireMouseDown](../vs140/COleControl--FireMouseDown.md)   
 [COleControl::FireMouseUp](../vs140/COleControl--FireMouseUp.md)