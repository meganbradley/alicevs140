---
title: "CMFCToolBar::SetLockedSizes"
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
ms.assetid: dfe882ab-dc53-4051-b038-b5aedfdeda82
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::SetLockedSizes
Sets the sizes of locked buttons and locked images on the toolbar.  
  
## Syntax  
  
```  
void SetLockedSizes(  
   SIZE sizeButton,  
   SIZE sizeImage,  
   BOOL bDontScale = FALSE  
);  
```  
  
#### Parameters  
 [in] `sizeButton`  
 Specifies the size of locked toolbar buttons.  
  
 [in] `sizeImage`  
 Specifies the size of locked toolbar images.  
  
 `bDontScale`  
 Specifies whether to scale or not locked toolbar images in high DPI mode.  
  
## Remarks  
 The default size of locked buttons is 23x22 pixels. The default size of locked images is 16x15 pixels.  
  
 Call the [CMFCToolBar::GetLockedImageSize](../vs140/CMFCToolBar--GetLockedImageSize.md) method to retrieve the size of locked images. Call the [CMFCToolBar::GetButtonSize](../vs140/CMFCToolBar--GetButtonSize.md) method to retrieve the size of locked toolbar buttons.  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBar::GetLockedImageSize](../vs140/CMFCToolBar--GetLockedImageSize.md)   
 [CMFCToolBar::GetButtonSize](../vs140/CMFCToolBar--GetButtonSize.md)