---
title: "CMFCToolBarButton::GetImage"
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
ms.assetid: 2fc70de0-4a7c-429a-8c27-5db81af1c394
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarButton::GetImage
Retrieves the image index of the button.  
  
## Syntax  
  
```  
int GetImage() const;  
```  
  
## Return Value  
 The index of the image associated with this button.  
  
## Remarks  
 If the button has a user-defined image (that is, if `bUserButton` was `TRUE` in the constructor), the returned index specifies an image in the collection of user-defined images (see [CMFCToolBar::GetUserImages](../vs140/CMFCToolBar--GetUserImages.md)). Otherwise, the index specifies an image in the collection of images that are loaded from a resource file (see [CMFCToolBar::GetImages](../vs140/CMFCToolBar--GetImages.md)). For more information about resource files, see [Working with Resource Files](../vs140/Working-with-Resource-Files.md).  
  
## Requirements  
 **Header:** afxtoolbarbutton.h  
  
## See Also  
 [CMFCToolBarButton Class](../vs140/CMFCToolBarButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBar::GetUserImages](../vs140/CMFCToolBar--GetUserImages.md)   
 [CMFCToolBar::GetImages](../vs140/CMFCToolBar--GetImages.md)   
 [Working with Resource Files](../vs140/Working-with-Resource-Files.md)