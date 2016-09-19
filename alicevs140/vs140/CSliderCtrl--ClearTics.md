---
title: "CSliderCtrl::ClearTics"
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
ms.assetid: 79cb04f9-3697-49a0-91af-50d576809ec2
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSliderCtrl::ClearTics
Removes the current tick marks from a slider control.  
  
## Syntax  
  
```  
  
      void ClearTics(  
   BOOL bRedraw = FALSE   
);  
```  
  
#### Parameters  
 `bRedraw`  
 Redraw flag. If this parameter is **TRUE**, the slider is redrawn after the tick marks are cleared; otherwise the slider is not redrawn.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CSliderCtrl Class](../vs140/CSliderCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CSliderCtrl::GetTicArray](../vs140/CSliderCtrl--GetTicArray.md)   
 [CSliderCtrl::GetTic](../vs140/CSliderCtrl--GetTic.md)   
 [CSliderCtrl::GetNumTics](../vs140/CSliderCtrl--GetNumTics.md)