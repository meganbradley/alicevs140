---
title: "COleControl::OnEnabledChanged"
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
ms.assetid: 2d54297b-8fc4-497e-a935-36d921be5997
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::OnEnabledChanged
Called by the framework when the stock Enabled property value has changed.  
  
## Syntax  
  
```  
  
virtual void OnEnabledChanged( );  
```  
  
## Remarks  
 Override this function if you want notification after this property changes. The default implementation calls [InvalidateControl](../vs140/COleControl--InvalidateControl.md).  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::SetEnabled](../vs140/COleControl--SetEnabled.md)   
 [COleControl::GetEnabled](../vs140/COleControl--GetEnabled.md)