---
title: "COleControl::OnKeyPressEvent"
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
ms.assetid: 3366347f-e792-4c2a-87c3-7c56041aeb72
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::OnKeyPressEvent
Called by the framework after the stock KeyPress event has been fired.  
  
## Syntax  
  
```  
  
      virtual void OnKeyPressEvent(  
   USHORT nChar   
);  
```  
  
#### Parameters  
 `nChar`  
 Contains the virtual key code value of the key pressed. For a list of standard virtual key codes, see Winuser.h  
  
## Remarks  
 Note that the `nChar` value may have been modified by the container.  
  
 Override this function if you want notification after this event occurs.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::FireKeyPress](../vs140/COleControl--FireKeyPress.md)