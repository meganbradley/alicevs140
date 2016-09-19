---
title: "CSliderCtrl::GetLineSize"
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
ms.assetid: a7f446b0-e6dd-4a2f-a1b8-e01569d6e69a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSliderCtrl::GetLineSize
Retrieves the size of the line for a slider control.  
  
## Syntax  
  
```  
  
int GetLineSize( ) const;  
```  
  
## Return Value  
 The size of a line for the slider control.  
  
## Remarks  
 The line size affects how much the slider moves for the **TB_LINEUP** and **TB_LINEDOWN** notifications. The default setting for the line size is 1.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CSliderCtrl Class](../vs140/CSliderCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CSliderCtrl::SetLineSize](../vs140/CSliderCtrl--SetLineSize.md)   
 [CSliderCtrl::GetPageSize](../vs140/CSliderCtrl--GetPageSize.md)