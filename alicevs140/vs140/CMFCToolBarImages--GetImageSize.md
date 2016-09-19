---
title: "CMFCToolBarImages::GetImageSize"
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
ms.assetid: 40cda928-92aa-4c74-b829-e07955dca5ca
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarImages::GetImageSize
Retrieves either the size of the toolbar images that are stored in memory (source size), or the size of the toolbar images that are drawn on the screen (destination size).  
  
## Syntax  
  
```  
SIZE GetImageSize(  
   BOOL bDest=FALSE   
) const;  
```  
  
#### Parameters  
 [in] `bDest`  
 `TRUE` to retrieve the destination size; `FALSE` to retrieve the source image size.  
  
## Return Value  
 A `SIZE` structure, which specifies the size of an image in pixels.  
  
## Remarks  
 The size of the source image is the size of the images that are stored in the [CMFCToolbarImages](../vs140/CMFCToolBarImages-Class.md) object. You can call [CMFCToolBarImages::SetImageSize](../vs140/CMFCToolBarImages--SetImageSize.md) to set the source size. The default value is 16x15 pixels.  
  
 By default, the destination image size is 0x0. You specify the destination size when you call [CMFCToolBarImages::PrepareDrawImage](../vs140/CMFCToolBarImages--PrepareDrawImage.md). The [CMFCToolBarImages::EndDrawImage](../vs140/CMFCToolBarImages--EndDrawImage.md) method resets the destination size to the default value.  
  
## Requirements  
 **Header:** afxtoolbarimages.h  
  
## See Also  
 [CMFCToolBarImages Class](../vs140/CMFCToolBarImages-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)