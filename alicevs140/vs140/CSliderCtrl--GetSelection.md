---
title: "CSliderCtrl::GetSelection"
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
ms.assetid: a3713032-0d90-4330-b73d-baad58562eed
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSliderCtrl::GetSelection
Retrieves the starting and ending positions of the current selection in a slider control.  
  
## Syntax  
  
```  
  
      void GetSelection(  
   int& nMin,  
   int& nMax   
) const;  
```  
  
#### Parameters  
 `nMin`  
 Reference to an integer that receives the starting position of the current selection.  
  
 `nMax`  
 Reference to an integer that receives the ending position of the current selection.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CSliderCtrl Class](../vs140/CSliderCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CSliderCtrl::SetSelection](../vs140/CSliderCtrl--SetSelection.md)   
 [CSliderCtrl::ClearSel](../vs140/CSliderCtrl--ClearSel.md)