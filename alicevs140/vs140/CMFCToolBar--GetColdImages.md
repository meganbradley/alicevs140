---
title: "CMFCToolBar::GetColdImages"
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
ms.assetid: 7f962f9a-cc95-458c-b073-67d5853fd5b6
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::GetColdImages
Returns a pointer to the collection of cold toolbar button images in the application.  
  
## Syntax  
  
```  
static CMFCToolBarImages* GetColdImages();  
```  
  
## Return Value  
 A pointer to the collection of cold toolbar button images.  
  
## Remarks  
 Cold images are the images that are used when the user is not interacting with the toolbar buttons. Call [LoadBitmapEx](../vs140/CMFCToolBar--LoadBitmapEx.md) or [CMFCToolBar::LoadBitmap](../vs140/CMFCToolBar--LoadBitmap.md) to load the cold images.  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [LoadBitmapEx](../vs140/CMFCToolBar--LoadBitmapEx.md)   
 [CMFCToolBar::LoadBitmap](../vs140/CMFCToolBar--LoadBitmap.md)