---
title: "CSliderCtrl::SetRangeMax"
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
ms.assetid: 564c5fe6-7059-4754-813f-aede2cc55044
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSliderCtrl::SetRangeMax
Sets the maximum range for the slider in a slider control.  
  
## Syntax  
  
```  
  
      void SetRangeMax(  
   int nMax,  
   BOOL bRedraw = FALSE   
);  
```  
  
#### Parameters  
 `nMax`  
 Maximum position for the slider.  
  
 `bRedraw`  
 The redraw flag. If this parameter is **TRUE**, the slider is redrawn after the range is set; otherwise the slider is not redrawn.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CSliderCtrl Class](../vs140/CSliderCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CSliderCtrl::SetRange](../vs140/CSliderCtrl--SetRange.md)   
 [CSliderCtrl::GetRangeMax](../vs140/CSliderCtrl--GetRangeMax.md)   
 [CSliderCtrl::SetRangeMin](../vs140/CSliderCtrl--SetRangeMin.md)