---
title: "CDrawingManager::FillGradient"
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
ms.assetid: 17b3f27f-8337-4c86-b636-d06cae253174
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDrawingManager::FillGradient
Fills a rectangular area with the specified color gradient.  
  
## Syntax  
  
```  
void FillGradient(  
   CRect rect,  
   COLORREF colorStart,  
   COLORREF colorFinish,  
   BOOL bHorz = TRUE,  
   int nStartFlatPercentage = 0,  
   int nEndFlatPercentage = 0  
);  
```  
  
#### Parameters  
 [in] `rect`  
 The rectangular area to fill.  
  
 [in] `colorStart`  
 The first color for the gradient.  
  
 [in] `colorFinish`  
 The final color for the gradient.  
  
 [in] `bHorz`  
 A Boolean parameter that specifies whether `FillGradient` should draw a horizontal or vertical gradient.  
  
 [in] `nStartFlatPercentage`  
 The percentage of the rectangle that `FillGradient` fills with `colorStart` before it starts the gradient.  
  
 [in] `nEndFlatPercentage`  
 The percentage of the rectangle that `FillGradient` fills with `colorFinish` after it finishes the gradient.  
  
## Example  
 The following example demonstrates how to use the `FillGradient` method of the `CDrawingManager` class. This code snippet is part of the [MS Office 2007 Demo sample](../vs140/Visual-C---Samples.md).  
  
 [!CODE [NVC_MFC_MSOffice2007Demo#12](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_MSOffice2007Demo#12)]  
  
## Requirements  
 **Header:** afxdrawmanager.h  
  
## See Also  
 [CDrawingManager Class](../vs140/CDrawingManager-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)