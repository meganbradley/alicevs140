---
title: "CMFCRibbonButton::GetImageIndex"
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
ms.assetid: c955a04c-202d-43b6-afcd-4de037e93f8e
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonButton::GetImageIndex
Returns the index of the image that is associated with the button.  
  
## Syntax  
  
```  
int GetImageIndex(  
   BOOL bLargeImage   
) const;  
```  
  
#### Parameters  
 [in] `bLargeImage`  
 If `TRUE`, returns the image index in the image list that contains the large images; otherwise returns the image index in the image list that contains the small images.  
  
## Return Value  
 The index of the button's image in the associated image list.  
  
## Requirements  
 **Header:** afxribbonbutton.h  
  
## See Also  
 [CMFCRibbonButton Class](../vs140/CMFCRibbonButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)