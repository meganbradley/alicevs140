---
title: "CDC::SetColorAdjustment"
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
ms.assetid: 3258d2bc-193e-4bbc-a36e-72b6f27ef708
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::SetColorAdjustment
Sets the color adjustment values for the device context using the specified values.  
  
## Syntax  
  
```  
  
      BOOL SetColorAdjustment(  
   const COLORADJUSTMENT* lpColorAdjust   
);  
```  
  
#### Parameters  
 `lpColorAdjust`  
 Points to a [COLORADJUSTMENT](../vs140/COLORADJUSTMENT-Structure.md) data structure containing the color adjustment values.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 The color adjustment values are used to adjust the input color of the source bitmap for calls to the `CDC::StretchBlt` member function when **HALFTONE** mode is set.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::SetStretchBltMode](../vs140/CDC--SetStretchBltMode.md)   
 [CDC::StretchBlt](../vs140/CDC--StretchBlt.md)   
 [StretchDIBits](http://msdn.microsoft.com/library/windows/desktop/dd145121)