---
title: "CMFCHeaderCtrl::IsMultipleSort"
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
ms.assetid: aafa2fb4-51b7-4fe4-be21-99e23c8bca6b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCHeaderCtrl::IsMultipleSort
Indicates whether the current header control is in *multiple column sort* mode.  
  
## Syntax  
  
```  
BOOL IsMultipleSort() const;  
```  
  
## Return Value  
 `TRUE` if multiple column sort mode is enabled; otherwise, `FALSE`.  
  
## Remarks  
 Use the [CMFCHeaderCtrl::EnableMultipleSort](../vs140/CMFCHeaderCtrl--EnableMultipleSort.md) method to enable or disable multiple column sort mode. Two or more columns can participate in a sort if the header control is in multiple column sort mode.  
  
## Requirements  
 **Header:** afxheaderctrl.h  
  
## See Also  
 [CMFCHeaderCtrl Class](../vs140/CMFCHeaderCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCHeaderCtrl::EnableMultipleSort](../vs140/CMFCHeaderCtrl--EnableMultipleSort.md)