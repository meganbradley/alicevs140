---
title: "COleControl::BoundPropertyRequestEdit"
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
ms.assetid: 1141ee71-f76a-4957-8f6c-df8a7e260ad3
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::BoundPropertyRequestEdit
Requests permission from the `IPropertyNotifySink` interface to change a bound property value provided by the control.  
  
## Syntax  
  
```  
  
      BOOL BoundPropertyRequestEdit(  
   DISPID dispid   
);  
```  
  
#### Parameters  
 `dispid`  
 The dispatch ID of a bound property of the control.  
  
## Return Value  
 Nonzero if the change is permitted; otherwise 0. The default value is nonzero.  
  
## Remarks  
 If permission is denied, the control must not let the value of the property change. This can be done by ignoring or failing the action that attempted to change the property value.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::BoundPropertyChanged](../vs140/COleControl--BoundPropertyChanged.md)