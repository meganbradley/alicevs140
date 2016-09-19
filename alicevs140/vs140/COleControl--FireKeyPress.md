---
title: "COleControl::FireKeyPress"
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
ms.assetid: c132b7d5-2bab-45cf-a40c-e9c18aa52304
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::FireKeyPress
Called by the framework when a key is pressed and released while the custom control is UI Active within the container.  
  
## Syntax  
  
```  
  
      void FireKeyPress(  
   USHORT* pnChar   
);  
```  
  
#### Parameters  
 `pnChar`  
 A pointer to the character value of the key pressed.  
  
## Remarks  
 If this event is defined as a custom event, you determine when the event is fired.  
  
 The recipient of the event may modify `pnChar`, for example, convert all lowercase characters to uppercase. If you want to examine the modified character, override `OnKeyPressEvent`.  
  
 For automatic firing of a KeyPress event to occur, the control's Event map must have a stock KeyPress event defined.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::OnKeyPressEvent](../vs140/COleControl--OnKeyPressEvent.md)   
 [COleControl::FireKeyDown](../vs140/COleControl--FireKeyDown.md)   
 [COleControl::FireKeyUp](../vs140/COleControl--FireKeyUp.md)