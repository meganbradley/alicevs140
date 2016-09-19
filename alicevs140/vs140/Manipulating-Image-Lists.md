---
title: "Manipulating Image Lists"
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
ms.assetid: 043418f8-077e-4dce-b8bb-2b7b0d7b5156
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Manipulating Image Lists
The [Replace](../vs140/CImageList--Replace.md) member function replaces an image in an image list ([CImageList](../vs140/CImageList-Class.md)) with a new image. This function is also useful if you need to dynamically increase the number of images in an image list object. The [SetImageCount](../vs140/CImageList--SetImageCount.md) function dynamically changes the number of images stored in the image list. If you increase the size of the image list, call **Replace** to add images to the new image slots. If you decrease the size of the image list, the images beyond the new size are freed.  
  
 The [Remove](../vs140/CImageList--Remove.md) member function removes an image from an image list. The [Copy](../vs140/CImageList--Copy.md) member function can copy or swap images within an image list. This function allows you to indicate whether the source image should be copied to the destination index or the source and destination images should be swapped.  
  
 To create a new image list by merging two image lists, use the appropriate overload of the [Create](../vs140/CImageList--Create.md) member function. This overload of **Create** merges the first image of the existing image lists, storing the resultant image in a new image list object. The new image is created by drawing the second image transparently over the first. The mask for the new image is the result of performing a logical-OR operation on the bits of the masks for the two existing images.  
  
 This is repeated until all images are merged and added to the new image list object.  
  
 You can write the image information to an archive by calling the [Write](../vs140/CImageList--Write.md) member function, and read it back by calling the [Read](../vs140/CImageList--Read.md) member function.  
  
 The [GetSafeHandle](../vs140/CImageList--GetSafeHandle.md), [Attach](../vs140/CImageList--Attach.md), and [Detach](../vs140/CImageList--Detach.md) member functions allow you to manipulate the handle of the image list attached to the `CImageList` object, while the [DeleteImageList](../vs140/CImageList--DeleteImageList.md) member function deletes the image list without destroying the `CImageList` object.  
  
## See Also  
 [Using CImageList](../vs140/Using-CImageList.md)   
 [Controls (MFC)](../vs140/Controls--MFC-.md)