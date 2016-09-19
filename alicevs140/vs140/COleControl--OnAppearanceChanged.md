---
title: "COleControl::OnAppearanceChanged"
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
ms.assetid: 2747d3f9-d02e-4c51-8f7e-5da6926b77cb
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::OnAppearanceChanged
Called by the framework when the stock Appearance property value has changed.  
  
## Syntax  
  
```  
  
virtual void OnAppearanceChanged ( );  
```  
  
## Remarks  
 Override this function if you want notification after this property changes. The default implementation calls `InvalidateControl`.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::GetAppearance](../vs140/COleControl--GetAppearance.md)   
 [COleControl::SetAppearance](../vs140/COleControl--SetAppearance.md)   
 [COleControl::InvalidateControl](../vs140/COleControl--InvalidateControl.md)