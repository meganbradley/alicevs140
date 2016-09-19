---
title: "CMFCToolBarImages::UpdateImage"
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
ms.assetid: daba1a66-2e55-4334-977d-af3c836fab43
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarImages::UpdateImage
Updates a user-defined toolbar image from a bitmap.  
  
## Syntax  
  
```  
BOOL UpdateImage(  
   int iImage,  
   HBITMAP hbmp   
);  
```  
  
#### Parameters  
 [in] `iImage`  
 The zero-based index of the image to update.  
  
 [in] `hbmp`  
 A handle to the bitmap from which to update the image.  
  
## Return Value  
 `TRUE` if the image was updated successfully; `FALSE` if the image list is not user-defined or temporary.  
  
## Requirements  
 **Header:** afxtoolbarimages.h  
  
## See Also  
 [CMFCToolBarImages Class](../vs140/CMFCToolBarImages-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)