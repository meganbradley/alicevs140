---
title: "CDC::GetColorAdjustment"
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
ms.assetid: a4b47c38-bf33-4fcd-a948-13dde5277b3a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::GetColorAdjustment
Retrieves the color adjustment values for the device context.  
  
## Syntax  
  
```  
  
      BOOL GetColorAdjustment(  
   LPCOLORADJUSTMENT lpColorAdjust   
) const;  
```  
  
#### Parameters  
 `lpColorAdjust`  
 Points to a [COLORADJUSTMENT](../vs140/COLORADJUSTMENT-Structure.md) data structure to receive the color adjustment values.  
  
## Return Value  
 Nonzero if the function is successful; otherwise 0.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::SetColorAdjustment](../vs140/CDC--SetColorAdjustment.md)