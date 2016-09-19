---
title: "CMFCToolBarButton::OnCalculateSize"
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
ms.assetid: 5c0a14b0-5fd5-4679-86a6-fde061caf6dd
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarButton::OnCalculateSize
Called by the framework to calculate the size of the button for the specified device context and docking state.  
  
## Syntax  
  
```  
virtual SIZE OnCalculateSize(  
   CDC* pDC,  
   const CSize& sizeDefault,  
   BOOL bHorz   
);  
```  
  
#### Parameters  
 [in] `pDC`  
 The device context that displays the button.  
  
 [in] `sizeDefault`  
 The default size of the button.  
  
 [in] `bHorz`  
 The dock state of the parent toolbar. This parameter is `TRUE` if the toolbar is docked horizontally or is floating, or `FALSE` if the toolbar is docked vertically.  
  
## Return Value  
 A `SIZE` structure that contains the dimensions of the button, in pixels.  
  
## Remarks  
 The framework calls this method to determine the size of the toolbar button for the specified device context and dock state.  
  
 The default implementation considers the text and image sizes (if they are displayed), the text and image positions (the text below or at the right-hand side of the image), and the toolbar dock state.  
  
 Override this method if you want to provide the size of a non-standard button (for example, an edit box button).  
  
## Requirements  
 **Header:** afxtoolbarbutton.h  
  
## See Also  
 [CMFCToolBarButton Class](../vs140/CMFCToolBarButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)