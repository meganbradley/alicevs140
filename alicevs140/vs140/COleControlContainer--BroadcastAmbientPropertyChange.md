---
title: "COleControlContainer::BroadcastAmbientPropertyChange"
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
ms.assetid: f547200a-33ed-45c3-90d2-8970912aeb3f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControlContainer::BroadcastAmbientPropertyChange
Informs all hosted controls that an ambient property has changed.  
  
## Syntax  
  
```  
  
      virtual void BroadcastAmbientPropertyChange(   
DISPID dispid   
);  
```  
  
#### Parameters  
 `dispid`  
 The dispatch ID of the ambient property being changed.  
  
## Remarks  
 This function is called by the framework when an ambient property has changed value. Override this function to customize this behavior.  
  
## Requirements  
 **Header:** afxocc.h  
  
## See Also  
 [COleControlContainer Class](../vs140/COleControlContainer-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::OnAmbientPropertyChange](../vs140/COleControl--OnAmbientPropertyChange.md)