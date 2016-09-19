---
title: "COleControl::FireDblClick"
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
ms.assetid: 6608cb8c-1bde-4ea1-aa00-7c0ee20a4c79
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::FireDblClick
Called by the framework when the mouse is double-clicked over an active control.  
  
## Syntax  
  
```  
  
void FireDblClick( );  
```  
  
## Remarks  
 If this event is defined as a custom event, you determine when the event is fired.  
  
 For automatic firing of a DblClick event to occur, the control's Event map must have a stock DblClick event defined.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::FireClick](../vs140/COleControl--FireClick.md)   
 [COleControl::FireMouseDown](../vs140/COleControl--FireMouseDown.md)   
 [COleControl::FireMouseUp](../vs140/COleControl--FireMouseUp.md)