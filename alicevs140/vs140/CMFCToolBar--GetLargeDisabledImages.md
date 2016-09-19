---
title: "CMFCToolBar::GetLargeDisabledImages"
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
ms.assetid: 94646734-bcce-4eba-b148-057d65b59be1
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::GetLargeDisabledImages
Returns a pointer to the collection of large disabled toolbar button images in the application.  
  
## Syntax  
  
```  
static CMFCToolBarImages* GetLargeDisabledImages();  
```  
  
## Return Value  
 A pointer to the collection of large disabled toolbar button images.  
  
## Remarks  
 Large images are large versions of the regular toolbar button images. Call [LoadBitmapEx](../vs140/CMFCToolBar--LoadBitmapEx.md) or [CMFCToolBar::LoadBitmap](../vs140/CMFCToolBar--LoadBitmap.md) to load the large images.  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [LoadBitmapEx](../vs140/CMFCToolBar--LoadBitmapEx.md)   
 [CMFCToolBar::LoadBitmap](../vs140/CMFCToolBar--LoadBitmap.md)