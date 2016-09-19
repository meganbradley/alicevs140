---
title: "Using CImageList"
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
ms.topic: article
ms.assetid: 3d2a909e-d641-46b7-aada-81cab1a29b41
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Using CImageList
An image list, represented by class [CImageList](../vs140/CImageList-Class.md), is a collection of same-sized images, each of which can be referred to by its index. Image lists are used to efficiently manage large sets of icons or bitmaps. Image lists are not themselves controls since they are not windows; however, they are used with several different types of controls, including list controls ([CListCtrl](../vs140/CListCtrl-Class.md)), tree controls ([CTreeCtrl](../vs140/CTreeCtrl-Class.md)), and tab controls ([CTabCtrl](../vs140/CTabCtrl-Class.md)).  
  
 All images in an image list are contained in a single, wide bitmap in screen-device format. An image list may also include a monochrome bitmap that contains masks used to draw images transparently (icon style). `CImageList` provides member functions that enable you to draw images, create and destroy image lists, add and remove images, replace images, merge images, and drag images.  
  
## What do you want to know more about?  
  
-   [Types of Image Lists](../vs140/Types-of-Image-Lists.md)  
  
-   [Using an Image List](../vs140/Using-an-Image-List.md)  
  
-   [Manipulating Image Lists](../vs140/Manipulating-Image-Lists.md)  
  
-   [Drawing Images from an Image List](../vs140/Drawing-Images-from-an-Image-List.md)  
  
-   [Image Overlays in Image Lists](../vs140/Image-Overlays-in-Image-Lists.md)  
  
-   [Dragging Images from an Image List](../vs140/Dragging-Images-from-an-Image-List.md)  
  
-   [Image Information in Image Lists](../vs140/Image-Information-in-Image-Lists.md)  
  
## See Also  
 [Controls (MFC)](../vs140/Controls--MFC-.md)