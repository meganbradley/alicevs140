---
title: "CMFCToolBar::GetUserImages"
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
ms.assetid: d91c7c85-64c2-4858-97fe-1a9771da9162
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::GetUserImages
Returns a pointer to the collection of user-defined toolbar button images in the application.  
  
## Syntax  
  
```  
static CMFCToolBarImages* GetUserImages();  
```  
  
## Return Value  
 A pointer to the collection of user-defined toolbar button images for all toolbars in the application.  
  
## Remarks  
 Call the [CMFCToolBar::SetUserImages](../vs140/CMFCToolBar--SetUserImages.md) method to set the collection of user-defined images in the application.  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBarImages Class](../vs140/CMFCToolBarImages-Class.md)   
 [CMFCToolBar::SetUserImages](../vs140/CMFCToolBar--SetUserImages.md)