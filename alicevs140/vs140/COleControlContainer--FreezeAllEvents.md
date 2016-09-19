---
title: "COleControlContainer::FreezeAllEvents"
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
ms.assetid: 1ffdf48b-2287-4bae-9076-f19b444413ff
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControlContainer::FreezeAllEvents
Determines if the container will ignore events from the attached control sites or accept them.  
  
## Syntax  
  
```  
  
      void FreezeAllEvents(  
   BOOL bFreeze   
);  
```  
  
#### Parameters  
 `bFreeze`  
 Nonzero if events will be processed; otherwise 0.  
  
## Remarks  
  
> [!NOTE]
>  The control is not required to stop firing events if requested by the control container. It can continue firing but all subsequent events will be ignored by the control container.  
  
## Requirements  
 **Header:** afxocc.h  
  
## See Also  
 [COleControlContainer Class](../vs140/COleControlContainer-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)