---
title: "CMFCVisualManagerOffice2003::OnDrawScrollButtons"
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
ms.assetid: 73b6d66b-cd9e-430c-abcc-80c65fd49930
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManagerOffice2003::OnDrawScrollButtons
The framework calls this method when it draws scroll buttons.  
  
## Syntax  
  
```  
virtual void OnDrawScrollButtons(  
   CDC* pDC,  
   const CRect& rect,  
   const int nBorderSize,  
   int iImage,  
   BOOL bHilited  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 Pointer to a device context.  
  
 [in] `rect`  
 The bounding rectangle of the scroll buttons.  
  
 [in] `nBorderSize`  
 The size of the border to draw around the scroll buttons.  
  
 [in] `iImage`  
 An identifier of the image to draw in the scroll buttons.  
  
 [in] `bHilited`  
 `TRUE` if the scroll buttons are highlighted, or `FALSE` if not.  
  
## Remarks  
  
## Requirements  
 **Header:** afxvisualmanageroffice2003.h  
  
## See Also  
 [CMFCVisualManagerOffice2003 Class](../vs140/CMFCVisualManagerOffice2003-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)