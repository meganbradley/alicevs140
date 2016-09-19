---
title: "COleControl::BoundPropertyChanged"
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
ms.assetid: 330bea4a-c138-4451-89bb-60365e5bb719
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::BoundPropertyChanged
Signals that the bound property value has changed.  
  
## Syntax  
  
```  
  
      void BoundPropertyChanged(  
   DISPID dispid   
);  
```  
  
#### Parameters  
 `dispid`  
 The dispatch ID of a bound property of the control.  
  
## Remarks  
 This must be called every time the value of the property changes, even in cases where the change was not made through the property Set method. Be particularly aware of bound properties that are mapped to member variables. Any time such a member variable changes, `BoundPropertyChanged` must be called.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::BoundPropertyRequestEdit](../vs140/COleControl--BoundPropertyRequestEdit.md)