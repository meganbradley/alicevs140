---
title: "CMFCRibbonEdit::HasCompactMode"
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
ms.assetid: 3f5427a5-4bd6-4710-8eed-6bcb94c377aa
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonEdit::HasCompactMode
Indicates whether the display size for the [CMFCRibbonEdit Class](../vs140/CMFCRibbonEdit-Class.md) control can be compact.  
  
## Syntax  
  
```  
virtual BOOL HasCompactMode() const;  
```  
  
## Return Value  
 Always returns `TRUE`.  
  
## Remarks  
 By default this method always returns `TRUE`. Override this method to indicate whether the display size can be compact.  
  
## Requirements  
 **Header:** afxribbonedit.h  
  
## See Also  
 [CMFCRibbonEdit Class](../vs140/CMFCRibbonEdit-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)