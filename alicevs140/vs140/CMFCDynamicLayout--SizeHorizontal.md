---
title: "CMFCDynamicLayout::SizeHorizontal"
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
ms.assetid: 3235c1a8-2810-4e7e-bc71-85744b87436d
caps.latest.revision: 6
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCDynamicLayout::SizeHorizontal
Gets a [SizeSettings](../vs140/CMFCDynamicLayout--SizeSettings-Structure.md) value that defines how much a child control is resized horizontally when the user resizes its hosting window.  
  
## Syntax  
  
```vb  
  
static SizeSettings SizeHorizontal(    int nRatio);  
```  
  
#### Parameters  
 `nRatio`  
 Defines as a percentage how far a child control is resized horizontally when the user resizes the host window.  
  
## Return Value  
 A [SizeSettings](../vs140/CMFCDynamicLayout--SizeSettings-Structure.md) value that encapsulates the requested size ratio.  
  
## Remarks  
  
## Requirements  
 **Header:** afxlayout.h  
  
## See Also  
 [CMFCDynamicLayout Class](../vs140/CMFCDynamicLayout-Class.md)   
 [CMFCDynamicLayout::SizeSettings Structure](../vs140/CMFCDynamicLayout--SizeSettings-Structure.md)