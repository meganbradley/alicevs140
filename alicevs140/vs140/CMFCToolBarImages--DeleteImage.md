---
title: "CMFCToolBarImages::DeleteImage"
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
ms.assetid: f2ea1169-3bdb-4da9-9676-2e9a8afd3f3f
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarImages::DeleteImage
Deletes the user-defined image that has a specified index from the toolbar images.  
  
## Syntax  
  
```  
BOOL DeleteImage(  
   int iImage   
);  
```  
  
#### Parameters  
 [in] `iImage`  
 Specifies the zero-based index of the image to delete.  
  
## Return Value  
 `TRUE` if the image was deleted successfully; `FALSE` if the image index is invalid, the `CMFCToolbarImages` object is temporary, the `CMFCToolbarImages` object does not contain user-defined images, or if some other error occurred.  
  
## Requirements  
 **Header:** afxtoolbarimages.h  
  
## See Also  
 [CMFCToolBarImages Class](../vs140/CMFCToolBarImages-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)