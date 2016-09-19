---
title: "COleControl::OnBorderStyleChanged"
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
ms.assetid: 1024a22d-6467-4753-97de-9f322aabe952
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::OnBorderStyleChanged
Called by the framework when the stock BorderStyle property value has changed.  
  
## Syntax  
  
```  
  
virtual void OnBorderStyleChanged( );  
```  
  
## Remarks  
 The default implementation calls `InvalidateControl`.  
  
 Override this function if you want notification after this property changes.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::SetBorderStyle](../vs140/COleControl--SetBorderStyle.md)   
 [COleControl::InvalidateControl](../vs140/COleControl--InvalidateControl.md)