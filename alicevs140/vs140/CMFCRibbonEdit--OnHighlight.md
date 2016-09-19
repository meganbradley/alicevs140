---
title: "CMFCRibbonEdit::OnHighlight"
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
ms.assetid: 4c45f8f6-7b39-4907-9d2f-68b79eb7a450
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonEdit::OnHighlight
Called by the framework when the pointer enters or leaves the bounds of the [CMFCRibbonEdit](../vs140/CMFCRibbonEdit-Class.md) control.  
  
## Syntax  
  
```  
virtual void OnHighlight(  
   BOOL bHighlight  
);  
```  
  
#### Parameters  
 [in] `bHighlight`  
 `TRUE` if the pointer is in the bounds of the [CMFCRibbonEdit](../vs140/CMFCRibbonEdit-Class.md) control; otherwise, `FALSE`.  
  
## Remarks  
  
## Requirements  
 **Header:** afxribbonedit.h  
  
## See Also  
 [CMFCRibbonEdit Class](../vs140/CMFCRibbonEdit-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)