---
title: "COleControl::OnHideToolBars"
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
ms.assetid: 20a4007f-74ec-4aff-ba74-1253d56b83c2
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::OnHideToolBars
Called by the framework when the control is UI deactivated.  
  
## Syntax  
  
```  
  
virtual void OnHideToolBars( );  
```  
  
## Remarks  
 The implementation should hide all toolbars displayed by `OnShowToolbars`.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::OnShowToolBars](../vs140/COleControl--OnShowToolBars.md)