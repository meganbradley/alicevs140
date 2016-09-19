---
title: "CMFCToolBarImages::GetImageWell"
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
ms.assetid: 0f354426-3333-4c9c-9ad2-70a0d298b0ee
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarImages::GetImageWell
Returns the handle to the bitmap that contains all the toolbar images.  
  
## Syntax  
  
```  
HBITMAP GetImageWell() const;  
```  
  
## Return Value  
 A handle to a bitmap that contains toolbar images.  
  
## Remarks  
 The toolbar images are stored in a row in a single bitmap that is known as an *image well*. To find a toolbar image in the image well, multiply the index of the image by the width of the toolbar images (see [CMFCToolBarImages::GetImageSize](../vs140/CMFCToolBarImages--GetImageSize.md)) to obtain the horizontal offset of the image inside the image well.  
  
## Requirements  
 **Header:** afxtoolbarimages.h  
  
## See Also  
 [CMFCToolBarImages Class](../vs140/CMFCToolBarImages-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)