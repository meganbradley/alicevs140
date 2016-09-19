---
title: "CMFCToolBar::GetDisabledImages"
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
ms.assetid: a68adeaa-94c3-45f3-83a0-82dd6d8065a5
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::GetDisabledImages
Returns a pointer to the collection of images that are used for disabled toolbar buttons in the application.  
  
## Syntax  
  
```  
static CMFCToolBarImages* __stdcall GetDisabledImages();  
```  
  
## Return Value  
 A pointer to the collection of disabled toolbar button images.  
  
## Remarks  
 Load the disabled toolbar button images by using the [CMFCToolBarEditBoxButton Class](../vs140/CMFCToolBarEditBoxButton-Class.md) and [CMFCToolBar::LoadBitmap](../vs140/CMFCToolBar--LoadBitmap.md) methods.  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBarEditBoxButton Class](../vs140/CMFCToolBarEditBoxButton-Class.md)   
 [CMFCToolBar::LoadBitmap](../vs140/CMFCToolBar--LoadBitmap.md)