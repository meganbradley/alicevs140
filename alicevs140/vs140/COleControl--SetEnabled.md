---
title: "COleControl::SetEnabled"
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
ms.assetid: 32006327-c927-44b0-83cb-95f43e34dbd6
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::SetEnabled
Sets the stock Enabled property value of your control.  
  
## Syntax  
  
```  
  
      void SetEnabled(  
   BOOL bEnabled   
);  
```  
  
#### Parameters  
 `bEnabled`  
 **TRUE** if the control is to be enabled; otherwise **FALSE**.  
  
## Remarks  
 After setting this property, **OnEnabledChange** is called.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::GetEnabled](../vs140/COleControl--GetEnabled.md)   
 [COleControl::OnEnabledChanged](../vs140/COleControl--OnEnabledChanged.md)