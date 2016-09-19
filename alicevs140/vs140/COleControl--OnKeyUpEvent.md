---
title: "COleControl::OnKeyUpEvent"
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
ms.assetid: c454cbd1-4f1a-437d-89a2-f930b1352f87
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::OnKeyUpEvent
Called by the framework after a stock KeyDown event has been processed.  
  
## Syntax  
  
```  
  
      virtual void OnKeyUpEvent(  
   USHORT nChar,  
   USHORT nShiftState   
);  
```  
  
#### Parameters  
 `nChar`  
 The virtual key code value of the pressed key. For a list of standard virtual key codes, see Winuser.h  
  
 `nShiftState`  
 Contains a combination of the following flags:  
  
-   **SHIFT_MASK** The SHIFT key was pressed during the action.  
  
-   **CTRL_MASK** The CTRL key was pressed during the action.  
  
-   **ALT_MASK** The ALT key was pressed during the action.  
  
## Remarks  
 Override this function if your control needs access to the key information after the event has been fired.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::OnKeyDownEvent](../vs140/COleControl--OnKeyDownEvent.md)   
 [COleControl::OnKeyPressEvent](../vs140/COleControl--OnKeyPressEvent.md)