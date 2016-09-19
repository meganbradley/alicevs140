---
title: "CSliderCtrl::GetRange"
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
ms.assetid: 483d1205-9db7-407f-ae3f-153eb3b040b2
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSliderCtrl::GetRange
Retrieves the maximum and minimum positions for the slider in a slider control.  
  
## Syntax  
  
```  
  
      void GetRange(  
   int& nMin,  
   int& nMax   
) const;  
```  
  
#### Parameters  
 `nMin`  
 Reference to an integer that receives the minimum position.  
  
 `nMax`  
 Reference to an integer that receives the maximum position.  
  
## Remarks  
 This function copies the values into the integers referenced by `nMin` and `nMax`.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CSliderCtrl Class](../vs140/CSliderCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CSliderCtrl::GetRangeMin](../vs140/CSliderCtrl--GetRangeMin.md)   
 [CSliderCtrl::GetRangeMax](../vs140/CSliderCtrl--GetRangeMax.md)   
 [CSliderCtrl::SetRange](../vs140/CSliderCtrl--SetRange.md)