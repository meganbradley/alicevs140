---
title: "CSliderCtrl::GetThumbRect"
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
ms.assetid: 708f8cc3-8d95-4f29-8cbb-2f4d1f46439d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSliderCtrl::GetThumbRect
Retrieves the size and position of the bounding rectangle for the slider (thumb) in a slider control.  
  
## Syntax  
  
```  
  
      void GetThumbRect(  
   LPRECT lprc   
) const;  
```  
  
#### Parameters  
 `lprc`  
 A pointer to a `CRect` object that contains the bounding rectangle for the slider when the function returns.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CSliderCtrl Class](../vs140/CSliderCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CSliderCtrl::GetChannelRect](../vs140/CSliderCtrl--GetChannelRect.md)