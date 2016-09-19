---
title: "CMFCToolBarImages::AddImage"
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
ms.assetid: 56136859-c9da-4a19-a77f-128fcc9da45e
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarImages::AddImage
Adds a bitmap to the toolbar images.  
  
## Syntax  
  
```  
int AddImage(  
   HBITMAP hbmp,  
   BOOL bSetBitPerPixel=FALSE   
);  
int AddImage(  
   const CMFCToolBarImages& imageList,  
   int nIndex   
);  
```  
  
#### Parameters  
 [in] `hbmp`  
 The handle to the bitmap to add.  
  
 [in] `bSetBitPerPixel`  
 `TRUE` if the [CMFCToolBarImages](../vs140/CMFCToolBarImages-Class.md) object uses the color depth (bits per pixel) of the new image; `FALSE` if the `CMFCToolbarImages` object keeps the current color depth.  
  
 [in] `imageList`  
 A reference to a `CMFCToolbarImages` object that contains the image to add.  
  
 [in] `nIndex`  
 The index in the source `CMFCToolbarImages` object of the image to add.  
  
## Return Value  
 The number of toolbar images that the [CMFCToolBarImages](../vs140/CMFCToolBarImages-Class.md) object maintains after the new bitmap was added successfully; -1 if the operation failed.  
  
## Requirements  
 **Header:** afxtoolbarimages.h  
  
## See Also  
 [CMFCToolBarImages Class](../vs140/CMFCToolBarImages-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)