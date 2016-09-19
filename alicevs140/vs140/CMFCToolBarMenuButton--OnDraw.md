---
title: "CMFCToolBarMenuButton::OnDraw"
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
ms.assetid: 0399ec23-2e2d-407f-936b-f88063cdfbbb
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarMenuButton::OnDraw
[!INCLUDE[cpp_fp_under_construction](../vs140/includes/cpp_fp_under_construction_md.md)]  
  
## Syntax  
  
```  
virtual void OnDraw(  
   CDC* pDC,  
   const CRect& rect,  
   CMFCToolBarImages* pImages,  
   BOOL bHorz = TRUE,  
   BOOL bCustomizeMode = FALSE,  
   BOOL bHighlight = FALSE,  
   BOOL bDrawBorder = TRUE,  
   BOOL bGrayDisabledButtons = TRUE  
);  
```  
  
#### Parameters  
 [in] `pDC`  
  [in] `rect`  
  [in] `pImages`  
  [in] `bHorz`  
  [in] `bCustomizeMode`  
  [in] `bHighlight`  
  [in] `bDrawBorder`  
  [in] `bGrayDisabledButtons`  
  
## Remarks  
  
## Requirements  
 **Header:** afxtoolbarmenubutton.h  
  
## See Also  
 [CMFCToolBarMenuButton Class](../vs140/CMFCToolBarMenuButton-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)