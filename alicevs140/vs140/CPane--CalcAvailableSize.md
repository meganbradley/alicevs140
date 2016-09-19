---
title: "CPane::CalcAvailableSize"
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
ms.assetid: 211a79cb-0faa-413a-938a-c5fab4e90224
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPane::CalcAvailableSize
Calculates the difference in size between a specified rectangle and the current window rectangle.  
  
## Syntax  
  
```  
virtual CSize CalcAvailableSize(  
   CRect rectRequired  
);  
```  
  
#### Parameters  
 [in] `rectRequired`  
 The required rectangle.  
  
## Return Value  
 The difference in width and height between `rectRequired` and the current window rectangle.  
  
## Requirements  
 **Header:** afxpane.h  
  
## See Also  
 [CPane Class](../vs140/CPane-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)