---
title: "CMFCRibbonCategory::GetImageCount"
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
ms.assetid: b25cb2fb-b3ab-4a9e-9de2-18d5131d16ba
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonCategory::GetImageCount
Retrieves the number of images in the specified image list that is contained in the ribbon category.  
  
## Syntax  
  
```  
int GetImageCount(  
   BOOL bIsLargeImage  
) const;  
```  
  
#### Parameters  
 [in] `bIsLargeImage`  
 `TRUE` for the number of images in the large image list; `FALSE` for the number of images in the small image list.  
  
## Return Value  
 The number of images in the specified image list.  
  
## Remarks  
  
## Requirements  
 **Header:** afxribboncategory.h  
  
## See Also  
 [CMFCRibbonCategory Class](../vs140/CMFCRibbonCategory-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)