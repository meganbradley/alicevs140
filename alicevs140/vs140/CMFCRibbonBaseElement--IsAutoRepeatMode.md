---
title: "CMFCRibbonBaseElement::IsAutoRepeatMode"
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
ms.assetid: d8452391-143f-4ab2-8a75-56653c9fab4c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonBaseElement::IsAutoRepeatMode
Indicates whether the ribbon element is in auto repeat mode.  
  
## Syntax  
  
```  
virtual BOOL IsAutoRepeatMode(  
    int& nDelay  
) const;  
```  
  
#### Parameters  
 [in] `nDelay`  
 This parameter is not used.  
  
## Return Value  
 Always returns `FALSE`.  
  
## Remarks  
 By default this method always returns `FALSE`. Override this method to indicate whether the ribbon element is in auto repeat mode.  
  
 In auto repeat mode, the ribbon element responds at a set interval, measured in milliseconds, to sustained user input.  
  
## Requirements  
 **Header:** afxbaseribbonelement.h  
  
## See Also  
 [CMFCRibbonBaseElement Class](../vs140/CMFCRibbonBaseElement-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CWnd::SetTimer](../vs140/CWnd--SetTimer.md)