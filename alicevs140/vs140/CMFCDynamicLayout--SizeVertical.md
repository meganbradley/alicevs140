---
title: "CMFCDynamicLayout::SizeVertical"
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
ms.assetid: 38570359-e805-4867-8185-d38b71c8df75
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCDynamicLayout::SizeVertical
Gets a [SizeSettings](../vs140/CMFCDynamicLayout--SizeSettings-Structure.md) value that defines how much a child control is resized vertically when the user resizes its hosting window.  
  
## Syntax  
  
```vb  
  
static SizeSettings SizeVertical(    int nRatio);  
```  
  
#### Parameters  
 `nRatio`  
 Defines as a percentage how far a child control is resized vertically when the user resizes the host window.  
  
## Return Value  
 A [SizeSettings](../vs140/CMFCDynamicLayout--SizeSettings-Structure.md) value that encapsulates the requested size ratio.  
  
## Remarks  
  
## Requirements  
 **Header:** afxlayout.h  
  
## See Also  
 [CMFCDynamicLayout Class](../vs140/CMFCDynamicLayout-Class.md)   
 [CMFCDynamicLayout::SizeSettings Structure](../vs140/CMFCDynamicLayout--SizeSettings-Structure.md)