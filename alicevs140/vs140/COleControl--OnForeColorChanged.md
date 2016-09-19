---
title: "COleControl::OnForeColorChanged"
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
ms.assetid: 85e96d59-f5af-4a35-87df-12ccd78debf6
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::OnForeColorChanged
Called by the framework when the stock ForeColor property value has changed.  
  
## Syntax  
  
```  
  
virtual void OnForeColorChanged( );  
```  
  
## Remarks  
 The default implementation calls `InvalidateControl`.  
  
 Override this function if you want notification after this property changes.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::SetForeColor](../vs140/COleControl--SetForeColor.md)   
 [COleControl::InvalidateControl](../vs140/COleControl--InvalidateControl.md)