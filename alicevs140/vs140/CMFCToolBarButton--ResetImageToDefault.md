---
title: "CMFCToolBarButton::ResetImageToDefault"
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
ms.assetid: 75ab7df4-8e0c-4ca0-b4dd-19cf9040fc37
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarButton::ResetImageToDefault
Sets to the default value the image that is associated with the button.  
  
## Syntax  
  
```  
virtual void ResetImageToDefault();  
```  
  
## Remarks  
 This method retrieves the default image from its parent toolbar by using the [CMFCToolBar::GetDefaultImage](../vs140/CMFCToolBar--GetDefaultImage.md) method. If the button has no associated default image, this method sets the text label of the button according to its string resource by using the [CStringT::LoadString](../vs140/CStringT--LoadString.md) method. For more information about string resources, see [Working with Resource Files](../vs140/Working-with-Resource-Files.md).  
  
 This method does nothing if the button has a user-defined image.  
  
## Requirements  
 **Header:** afxtoolbarbutton.h  
  
## See Also  
 [CMFCToolBarButton Class](../vs140/CMFCToolBarButton-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBar::GetDefaultImage](../vs140/CMFCToolBar--GetDefaultImage.md)   
 [CStringT::LoadString](../vs140/CStringT--LoadString.md)   
 [Working with Resource Files](../vs140/Working-with-Resource-Files.md)