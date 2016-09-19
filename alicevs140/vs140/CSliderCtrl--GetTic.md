---
title: "CSliderCtrl::GetTic"
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
ms.assetid: 5bcfaccc-90c9-48fd-990d-a4e44b5eb25d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSliderCtrl::GetTic
Retrieves the position of a tick mark in a slider control.  
  
## Syntax  
  
```  
  
      int GetTic(  
   int nTic   
) const;  
```  
  
#### Parameters  
 `nTic`  
 Zero-based index identifying a tick mark.  
  
## Return Value  
 The position of the specified tick mark or – 1 if `nTic` does not specify a valid index.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CSliderCtrl Class](../vs140/CSliderCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CSliderCtrl::SetTic](../vs140/CSliderCtrl--SetTic.md)   
 [CSliderCtrl::GetTicArray](../vs140/CSliderCtrl--GetTicArray.md)   
 [CSliderCtrl::GetTicPos](../vs140/CSliderCtrl--GetTicPos.md)   
 [CSliderCtrl::SetTicFreq](../vs140/CSliderCtrl--SetTicFreq.md)   
 [CSliderCtrl::ClearTics](../vs140/CSliderCtrl--ClearTics.md)