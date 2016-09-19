---
title: "CMFCToolBar::GetLockedMenuImages"
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
ms.assetid: 3f7b6f57-bcd1-489f-9616-2f2eb6d866dc
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::GetLockedMenuImages
Returns a pointer to the collection of locked toolbar menu images in the toolbar.  
  
## Syntax  
  
```  
CMFCToolBarImages* GetLockedMenuImages();  
```  
  
## Return Value  
 A pointer to the collection of locked toolbar menu images, or `NULL` if the toolbar is not locked.  
  
## Remarks  
 Locked images are versions of the regular toolbar menu images that the framework uses when the user cannot customize the toolbar.  
  
 This method returns `NULL` if the toolbar is not locked. This method also generates an assertion failure in Debug builds if the toolbar is not locked. For more information about locked toolbars, see [CMFCToolBar::IsLocked](../vs140/CMFCToolBar--IsLocked.md).  
  
 Call the [CMFCToolBar::LoadBitmapEx](../vs140/CMFCToolBar--LoadBitmapEx.md) method to load the locked menu images.  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBar::IsLocked](../vs140/CMFCToolBar--IsLocked.md)   
 [CMFCToolBar::LoadBitmapEx](../vs140/CMFCToolBar--LoadBitmapEx.md)