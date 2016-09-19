---
title: "CMFCToolBar::GetLockedImageSize"
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
ms.assetid: 0193b7e2-777d-4a15-9b80-2e47ac0987b2
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::GetLockedImageSize
Returns the default size of locked toolbar images.  
  
## Syntax  
  
```  
CSize GetLockedImageSize() const;  
```  
  
## Return Value  
 A `CSize` structure that specifies the size of locked toolbar images or an empty `CSize` structure if the toolbar is not locked.  
  
## Remarks  
 Locked images are versions of the regular toolbar button images that the framework uses when the user cannot customize the toolbar.  
  
 This method returns a `CSize` structure with zero width and zero height if the toolbar is not locked. This method also generates an assertion failure in Debug builds if the toolbar is not locked. For more information about locked toolbars, see [CMFCToolBar::IsLocked](../vs140/CMFCToolBar--IsLocked.md).  
  
 Call the [CMFCToolBar::SetLockedSizes](../vs140/CMFCToolBar--SetLockedSizes.md) method to specify the locked image size.  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBar::IsLocked](../vs140/CMFCToolBar--IsLocked.md)   
 [CMFCToolBar::SetLockedSizes](../vs140/CMFCToolBar--SetLockedSizes.md)