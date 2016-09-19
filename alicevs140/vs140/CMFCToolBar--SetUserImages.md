---
title: "CMFCToolBar::SetUserImages"
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
ms.assetid: 6f24bff2-121d-4044-925f-4f45709fcc80
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::SetUserImages
Sets the collection of user-defined images in the application.  
  
## Syntax  
  
```  
static BOOL SetUserImages(  
   CMFCToolBarImages* pUserImages   
);  
```  
  
#### Parameters  
 [in] `pUserImages`  
 A pointer to the collection of user-defined images.  
  
## Return Value  
 Nonzero if the method succeeds; otherwise 0 if the specified `CMFCToolBarImages` object is not valid or has an image size that differs from the default image size of the toolbar.  
  
## Remarks  
 The framework uses user-defined images to draw toolbar buttons that are customized by the user. The image list specified by `pUserImages` is shared among all toolbars in the application.  
  
 This method generates an assertion failure in Debug builds if the specified `CMFCToolBarImages` object is not valid or has an image size that differs from the default image size of the toolbar.  
  
 The OutlookDemo, ToolTipDemo, and VisualStudioDemo samples use this method to set the global collection of user-defined images. They load the file that is named UserImages.bmp, which is located in the working directory of the application.  
  
 Call the [CMFCToolBar::GetUserImages](../vs140/CMFCToolBar--GetUserImages.md) method to retrieve the collection of user-defined images in the application.  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBarImages Class](../vs140/CMFCToolBarImages-Class.md)   
 [CMFCToolBar::GetUserImages](../vs140/CMFCToolBar--GetUserImages.md)