---
title: "CMFCToolBar::GetImages"
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
ms.assetid: 515b8334-9e62-4bed-8dab-2215fe37e593
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::GetImages
Returns a pointer to the collection of default button images in the application.  
  
## Syntax  
  
```  
static CMFCToolBarImages* GetImages();  
```  
  
## Return Value  
 A pointer to the [CMFCToolBarImages Class](../vs140/CMFCToolBarImages-Class.md) object that contains the collection of default images for all toolbars in the application.  
  
## Remarks  
 This shared method provides access to the collection of all default toolbar images for the application. Call the [CMFCToolBar::LoadBitmap](../vs140/CMFCToolBar--LoadBitmap.md) method to add images to the collection.  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBarImages Class](../vs140/CMFCToolBarImages-Class.md)   
 [CMFCToolBar::LoadBitmap](../vs140/CMFCToolBar--LoadBitmap.md)