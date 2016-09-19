---
title: "COleControl::ControlInfoChanged"
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
ms.assetid: 775db140-ac89-4afd-84fc-54146e2b397c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::ControlInfoChanged
Call this function when the set of mnemonics supported by the control has changed.  
  
## Syntax  
  
```  
  
void ControlInfoChanged( );  
```  
  
## Remarks  
 Upon receiving this notification, the control's container obtains the new set of mnemonics by making a call to [IOleControl::GetControlInfo](http://msdn.microsoft.com/library/windows/desktop/ms693730). Note that the container is not required to respond to this notification.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)