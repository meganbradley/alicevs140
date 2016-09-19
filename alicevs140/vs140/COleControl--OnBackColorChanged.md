---
title: "COleControl::OnBackColorChanged"
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
ms.assetid: 40890ef1-d124-4e7e-a810-439c2cdf8b48
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::OnBackColorChanged
Called by the framework when the stock BackColor property value has changed.  
  
## Syntax  
  
```  
  
virtual void OnBackColorChanged( );  
```  
  
## Remarks  
 Override this function if you want notification after this property changes. The default implementation calls `InvalidateControl`.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::GetBackColor](../vs140/COleControl--GetBackColor.md)   
 [COleControl::InvalidateControl](../vs140/COleControl--InvalidateControl.md)