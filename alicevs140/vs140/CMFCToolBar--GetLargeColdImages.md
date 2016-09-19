---
title: "CMFCToolBar::GetLargeColdImages"
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
ms.assetid: 210d9070-f72f-4fac-b356-3fd6eb0efae8
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::GetLargeColdImages
Returns a pointer to the collection of large cold toolbar button images in the application.  
  
## Syntax  
  
```  
static CMFCToolBarImages* GetLargeColdImages();  
```  
  
## Return Value  
 A pointer to the collection of large cold images.  
  
## Remarks  
 Cold images are the images that are used when the user is not interacting with the toolbar buttons. Call [LoadBitmapEx](../vs140/CMFCToolBar--LoadBitmapEx.md) to load the large cold images.  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [LoadBitmapEx](../vs140/CMFCToolBar--LoadBitmapEx.md)