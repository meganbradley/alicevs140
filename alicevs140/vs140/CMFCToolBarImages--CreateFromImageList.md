---
title: "CMFCToolBarImages::CreateFromImageList"
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
ms.assetid: d38958f3-bab1-4630-9fdc-b91cb974d334
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarImages::CreateFromImageList
Initializes the toolbar images from a [CImageList](../vs140/CImageList-Class.md) object.  
  
## Syntax  
  
```  
BOOL CreateFromImageList(  
   const CImageList& imageList   
);  
```  
  
#### Parameters  
 [in] `imageList`  
 The image list to be used as a source for toolbar images.  
  
## Return Value  
 Always returns `TRUE`.  
  
## Remarks  
 Use this function to quickly initialize the toolbar images list from an external image list.  
  
## Requirements  
 **Header:** afxtoolbarimages.h  
  
## See Also  
 [CMFCToolBarImages Class](../vs140/CMFCToolBarImages-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)