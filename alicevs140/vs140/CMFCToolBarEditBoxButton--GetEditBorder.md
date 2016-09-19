---
title: "CMFCToolBarEditBoxButton::GetEditBorder"
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
ms.assetid: 8fb5c348-5657-449a-b75a-24ea0b2535f6
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarEditBoxButton::GetEditBorder
Retrieves the bounding rectangle of the edit part of the edit box button.  
  
## Syntax  
  
```  
virtual void GetEditBorder(  
   CRect& rectBorder  
);  
```  
  
#### Parameters  
 [out] `rectBorder`  
 A reference to the `CRect` object that receives the bounding rectangle.  
  
## Remarks  
 This method retrieves the bounding rectangle of the edit control in client coordinates. It expands the size of the rectangle in each direction by one pixel.  
  
 The [CMFCVisualManager::OnDrawEditBorder](../vs140/CMFCVisualManager--OnDrawEditBorder.md) method calls this method when it draws the border around a `CMFCToolBarEditBoxButton` object.  
  
## Requirements  
 **Header:** afxtoolbareditboxbutton.h  
  
## See Also  
 [CMFCToolBarEditBoxButton Class](../vs140/CMFCToolBarEditBoxButton-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCVisualManager::OnDrawEditBorder](../vs140/CMFCVisualManager--OnDrawEditBorder.md)