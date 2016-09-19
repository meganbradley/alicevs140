---
title: "CMFCToolBar::SetMenuSizes"
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
ms.assetid: 0b5434c1-3f48-4ea0-821d-b67ed20bab84
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::SetMenuSizes
Sets the size of toolbar menu buttons and their images.  
  
## Syntax  
  
```  
static void __stdcall SetMenuSizes(  
   SIZE sizeButton,  
   SIZE sizeImage   
);  
```  
  
#### Parameters  
 [in] `sizeButton`  
 Specifies the size of toolbar buttons, in pixels.  
  
 [in] `sizeImage`  
 Specifies the size of toolbar images, in pixels.  
  
## Remarks  
 By default, menu buttons and their images have an undefined size.  
  
 Call the [CMFCToolBar::GetMenuButtonSize](../vs140/CMFCToolBar--GetMenuButtonSize.md) method to determine the size of menu buttons and the [CMFCToolBar::GetMenuImageSize](../vs140/CMFCToolBar--GetMenuImageSize.md) method to determine the size of menu button images.  
  
 See the IEDemo and MSMoneyDemo samples for examples that use this method.  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBar::GetMenuButtonSize](../vs140/CMFCToolBar--GetMenuButtonSize.md)   
 [CMFCToolBar::GetMenuImageSize](../vs140/CMFCToolBar--GetMenuImageSize.md)