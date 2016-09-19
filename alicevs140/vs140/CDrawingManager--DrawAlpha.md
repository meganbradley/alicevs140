---
title: "CDrawingManager::DrawAlpha"
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
ms.assetid: 290189c1-3eef-46bf-8768-9641383a981c
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDrawingManager::DrawAlpha
Displays bitmaps that have transparent or semitransparent pixels.  
  
## Syntax  
  
```  
void DrawAlpha(  
   CDC* pDstDC,  
   const CRect& rectDst,  
   CDC* pSrcDC,  
   const CRect& rectSrc  
);  
```  
  
#### Parameters  
 [in] `pDstDC`  
 A pointer to the device context for the destination.  
  
 [in] `rectDst`  
 The destination rectangle.  
  
 [in] `pSrcDC`  
 A pointer to the device context for the source.  
  
 [in] `rectSrc`  
 The source rectangle.  
  
## Remarks  
 This method performs alpha-blending for two bitmaps. For more information about alpha-blending, see [AlphaBlend](http://msdn.microsoft.com/library/windows/desktop/dd183351) in the Windows SDK.  
  
## Requirements  
 **Header:** afxdrawmanager.h  
  
## See Also  
 [CDrawingManager Class](../vs140/CDrawingManager-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)