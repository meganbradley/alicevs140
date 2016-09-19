---
title: "CMFCImagePaintArea::SetBitmap"
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
ms.assetid: abe405b6-68a1-4f27-848e-ba57b0148797
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCImagePaintArea::SetBitmap
Sets the bitmap image for the picture area.  
  
## Syntax  
  
```  
void SetBitmap(  
   CBitmap* pBitmap  
);  
```  
  
#### Parameters  
  
|||  
|-|-|  
|Parameter|Description|  
|[in] `pBitmap`|The new bitmap image to display.|  
  
## Remarks  
 If `pBitmap` is `NULL`, this method sets the size of the modifiable paint area to zero. Otherwise, it sets the size of the modifiable paint area to the size of the provided bitmap image.  
  
## Requirements  
 **Header:** afximagepaintarea.h  
  
## See Also  
 [CMFCImagePaintArea Class](../vs140/CMFCImagePaintArea-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CBitmap Class](../vs140/CBitmap-Class.md)