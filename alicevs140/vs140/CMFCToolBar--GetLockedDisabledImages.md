---
title: "CMFCToolBar::GetLockedDisabledImages"
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
ms.assetid: bed1e0ee-5755-4769-b56f-de6325eb47c7
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::GetLockedDisabledImages
Returns a pointer to the collection of locked disabled images in the toolbar.  
  
## Syntax  
  
```  
CMFCToolBarImages* GetLockedDisabledImages();  
```  
  
## Return Value  
 A pointer to the collection of locked disabled images, or `NULL` if the toolbar is not locked.  
  
## Remarks  
 Locked images are versions of the regular toolbar button images that the framework uses when the user cannot customize the toolbar. Disabled images are the images that the framework uses when a button has the `TBBS_DISABLED` style.  
  
 This method returns `NULL` if the toolbar is not locked. This method also generates an assertion failure in Debug builds if the toolbar is not locked. For more information about locked toolbars, see [CMFCToolBar::IsLocked](../vs140/CMFCToolBar--IsLocked.md).  
  
 Call the [CMFCToolBar::LoadBitmapEx](../vs140/CMFCToolBar--LoadBitmapEx.md) method to load the locked disabled images.  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBar::IsLocked](../vs140/CMFCToolBar--IsLocked.md)   
 [CMFCToolBar::LoadBitmapEx](../vs140/CMFCToolBar--LoadBitmapEx.md)