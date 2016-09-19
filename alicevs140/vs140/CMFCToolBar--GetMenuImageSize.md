---
title: "CMFCToolBar::GetMenuImageSize"
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
ms.assetid: 4f131077-5201-42ab-b83b-43086a293dbd
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::GetMenuImageSize
Returns the size of menu button images in the application.  
  
## Syntax  
  
```  
static CSize GetMenuImageSize();  
```  
  
## Return Value  
 A `CSize` object that represents the size of menu images.  
  
## Remarks  
 This method returns the size of images on toolbar menu buttons that is maintained as a global variable. Call [CMFCToolBar::SetMenuSizes](../vs140/CMFCToolBar--SetMenuSizes.md) to set this global variable.  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)