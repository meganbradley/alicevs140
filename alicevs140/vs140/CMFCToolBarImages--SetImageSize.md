---
title: "CMFCToolBarImages::SetImageSize"
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
ms.assetid: aea68c4f-ec9e-45db-aa91-47086292fc61
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarImages::SetImageSize
Sets the size of each toolbar image (source size).  
  
## Syntax  
  
```  
void SetImageSize(  
   SIZE sizeImage,  
   BOOL bUpdateCount=FALSE   
);  
```  
  
#### Parameters  
 [in] `sizeImage`  
 The new size of toolbar images.  
  
## Remarks  
 By default the size of the toolbar image is 16x15 pixels. Call this method if you want to use toolbar images of a different size.  
  
## Requirements  
 **Header:** afxtoolbarimages.h  
  
## See Also  
 [CMFCToolBarImages Class](../vs140/CMFCToolBarImages-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)