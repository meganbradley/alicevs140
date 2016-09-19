---
title: "CSliderCtrl::SetRange"
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
ms.assetid: 9c6432aa-1d21-43a3-8d0c-51827d5d18ca
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSliderCtrl::SetRange
Sets the range (minimum and maximum positions) for the slider in a slider control.  
  
## Syntax  
  
```  
  
      void SetRange(  
   int nMin,  
   int nMax,  
   BOOL bRedraw = FALSE   
);  
```  
  
#### Parameters  
 `nMin`  
 Minimum position for the slider.  
  
 `nMax`  
 Maximum position for the slider.  
  
 `bRedraw`  
 The redraw flag. If this parameter is **TRUE**, the slider is redrawn after the range is set; otherwise the slider is not redrawn.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CSliderCtrl Class](../vs140/CSliderCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CSliderCtrl::GetRange](../vs140/CSliderCtrl--GetRange.md)   
 [CSliderCtrl::SetRangeMax](../vs140/CSliderCtrl--SetRangeMax.md)   
 [CSliderCtrl::SetRangeMin](../vs140/CSliderCtrl--SetRangeMin.md)