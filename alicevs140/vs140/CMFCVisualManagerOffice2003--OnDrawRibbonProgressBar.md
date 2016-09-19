---
title: "CMFCVisualManagerOffice2003::OnDrawRibbonProgressBar"
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
ms.assetid: b174cca7-7733-4627-bb79-9f5cefa611bf
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManagerOffice2003::OnDrawRibbonProgressBar
The framework calls this method when it draws a [CMFCRibbonProgressBar](../vs140/CMFCRibbonProgressBar-Class.md)object.  
  
## Syntax  
  
```  
virtual void OnDrawRibbonProgressBar(  
   CDC* pDC,  
   CMFCRibbonProgressBar* pProgress,  
   CRect rectProgress,  
   CRect rectChunk,  
   BOOL bInfiniteMode  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context.  
  
 [in] `pProgress`  
 A pointer to a [CMFCRibbonProgressBar](../vs140/CMFCRibbonProgressBar-Class.md) object. The framework draws this progress bar.  
  
 [in] `rectProgress`  
 A rectangle that specifies the boundaries of the progress bar.  
  
 [in] `rectChunk`  
 A rectangle that specifies the boundaries of the area surrounding the progress bar.  
  
 [in] `bInfiniteMode`  
 `TRUE` if the bar is in infinite mode, or `FALSE` if not. The default implementation does not use this parameter.  
  
## Remarks  
 Override this method in a derived class to customize the appearance of a progress bar  
  
## Requirements  
 **Header:** afxvisualmanageroffice2003.h  
  
## See Also  
 [CMFCVisualManagerOffice2003 Class](../vs140/CMFCVisualManagerOffice2003-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)