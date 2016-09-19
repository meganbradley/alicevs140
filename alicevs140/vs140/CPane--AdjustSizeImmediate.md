---
title: "CPane::AdjustSizeImmediate"
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
ms.assetid: e5d17da3-dd4b-4708-be99-9edf40fc0121
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPane::AdjustSizeImmediate
Immediately recalculates the layout of a pane.  
  
## Syntax  
  
```  
virtual void AdjustSizeImmediate(  
   BOOL bRecalcLayout = TRUE  
);  
```  
  
#### Parameters  
 [in] `bRecalcLayout`  
 `TRUE` to automatically recalculate the layout of the pane; otherwise, `FALSE`.  
  
## Remarks  
 Call this method when you dynamically change the layout of a pane. For example, you may want to call this method when you hide or show toolbar buttons.  
  
## Requirements  
 **Header:** afxPane.h  
  
## See Also  
 [CPane Class](../vs140/CPane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)