---
title: "CMFCToolBar::GetMenuImages"
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
ms.assetid: 640d596e-bc48-4801-9712-0a3da54e3e84
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::GetMenuImages
Returns a pointer to the collection of menu button images in the application.  
  
## Syntax  
  
```  
static CMFCToolBarImages* GetMenuImages();  
```  
  
## Return Value  
 A pointer to the collection of menu images.  
  
## Remarks  
 Call the [LoadBitmapEx](../vs140/CMFCToolBar--LoadBitmapEx.md) method to load the menu images.  
  
 Call the [CMFCToolBar::SetMenuSizes](../vs140/CMFCToolBar--SetMenuSizes.md) method to set the size of buttons and their images.  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [LoadBitmapEx](../vs140/CMFCToolBar--LoadBitmapEx.md)   
 [CMFCToolBar::SetMenuSizes](../vs140/CMFCToolBar--SetMenuSizes.md)