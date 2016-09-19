---
title: "CMFCToolBar::SetSizes"
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
ms.assetid: 46be0f44-a140-474d-bd8a-34b6847aaf5a
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::SetSizes
Specifies the sizes of buttons and images on all toolbars.  
  
## Syntax  
  
```  
static void __stdcall SetSizes(  
   SIZE sizeButton,  
   SIZE sizeImage   
);  
```  
  
#### Parameters  
 [in] `sizeButton`  
 The size of toolbar buttons, in pixels.  
  
 [in] `sizeImage`  
 The size of toolbar button images, in pixels.  
  
## Remarks  
 The default size of toolbar buttons is 23x22 pixels. The default size of toolbar button images is 16x15 pixels.  
  
 Call the [CMFCToolBar::GetImageSize](../vs140/CMFCToolBar--GetImageSize.md) method to retrieve the size of toolbar button images. Call the [CMFCToolBar::GetButtonSize](../vs140/CMFCToolBar--GetButtonSize.md) method to retrieve the size of toolbar buttons.  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBar::GetImageSize](../vs140/CMFCToolBar--GetImageSize.md)   
 [CMFCToolBar::GetButtonSize](../vs140/CMFCToolBar--GetButtonSize.md)