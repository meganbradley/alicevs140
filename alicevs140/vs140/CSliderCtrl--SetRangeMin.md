---
title: "CSliderCtrl::SetRangeMin"
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
ms.assetid: 4fb82b02-d236-43a4-bb3e-b9854dae49d5
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSliderCtrl::SetRangeMin
Sets the minimum range for the slider in a slider control.  
  
## Syntax  
  
```  
  
      void SetRangeMin(  
   int nMin,  
   BOOL bRedraw = FALSE   
);  
```  
  
#### Parameters  
 `nMin`  
 Minimum position for the slider.  
  
 `bRedraw`  
 The redraw flag. If this parameter is **TRUE**, the slider is redrawn after the range is set; otherwise the slider is not redrawn.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CSliderCtrl Class](../vs140/CSliderCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CSliderCtrl::SetRange](../vs140/CSliderCtrl--SetRange.md)   
 [CSliderCtrl::GetRangeMin](../vs140/CSliderCtrl--GetRangeMin.md)   
 [CSliderCtrl::SetRangeMax](../vs140/CSliderCtrl--SetRangeMax.md)