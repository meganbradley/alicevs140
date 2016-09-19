---
title: "Image Information in Image Lists"
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
ms.assetid: 73c41543-fa91-405d-b15b-0feffa6a72c1
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Image Information in Image Lists
[CImageList](../vs140/CImageList-Class.md) includes a number of functions that retrieve information from an image list. The [GetImageInfo](../vs140/CImageList--GetImageInfo.md) member function fills an `IMAGEINFO` structure with information about a single image, including the handles of the image and mask bitmaps, the number of color planes and bits per pixel, and the bounding rectangle of the image within the image bitmap. You can use this information to directly manipulate the bitmaps for the image.  
  
 The [GetImageCount](../vs140/CImageList--GetImageCount.md) member function retrieves the number of images in an image list.  
  
 You can create an icon based on an image and mask in an image list by using the [ExtractIcon](../vs140/CImageList--ExtractIcon.md) member function. The function returns the handle of the new icon.  
  
## See Also  
 [Using CImageList](../vs140/Using-CImageList.md)   
 [Controls (MFC)](../vs140/Controls--MFC-.md)