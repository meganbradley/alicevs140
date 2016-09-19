---
title: "CMFCToolBarButton::SetImage"
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
ms.assetid: 17b33020-ac0e-4dc2-9514-146bf0d4eb1b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarButton::SetImage
Sets the image index of the button.  
  
## Syntax  
  
```  
virtual void SetImage(  
   int iImage   
);  
```  
  
#### Parameters  
 [in] `iImage`  
 The index of the image in the collection of toolbar images.  
  
## Remarks  
 If the toolbar button is a separator, `iImage` refers to the new width of the separator button.  
  
 If `iImage` is less than zero, this method disables drawing of the image and enables drawing of the text label of the button.  
  
## Requirements  
 **Header:** afxtoolbarbutton.h  
  
## See Also  
 [CMFCToolBarButton Class](../vs140/CMFCToolBarButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBarButton::GetImage](../vs140/CMFCToolBarButton--GetImage.md)