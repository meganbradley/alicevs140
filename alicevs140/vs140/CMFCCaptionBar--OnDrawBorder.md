---
title: "CMFCCaptionBar::OnDrawBorder"
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
ms.assetid: 40144ffe-1fb4-463e-aed6-120fdda7b5da
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCCaptionBar::OnDrawBorder
Called by the framework to draw the border of the caption bar.  
  
## Syntax  
  
```  
virtual void OnDrawBorder(  
   CDC* pDC,  
   CRect rect   
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A device context that is used to display the borders.  
  
 [in] `rect`  
 The bounding rectangle.  
  
## Remarks  
 By default, the borders have the flat style.  
  
 Override this method in a `CMFCCaptionBar` derived class to customize the appearance of the caption bar's borders.  
  
## Requirements  
 **Header:** afxcaptionbar.h  
  
## See Also  
 [CMFCCaptionBar Class](../vs140/CMFCCaptionBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)