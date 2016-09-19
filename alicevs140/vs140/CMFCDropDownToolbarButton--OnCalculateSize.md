---
title: "CMFCDropDownToolbarButton::OnCalculateSize"
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
ms.assetid: 24fde7fb-ee85-4ae6-8979-d0a904ae2f96
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCDropDownToolbarButton::OnCalculateSize
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
 This method extends the base class implementation ([CMFCToolBarButton::OnCalculateSize](../vs140/CMFCToolBarButton--OnCalculateSize.md)) by adding the width of the drop-down arrow to the horizontal dimension of the button size.  
  
## Requirements  
 **Header:** afxdropdowntoolbar.h  
  
## See Also  
 [CMFCDropDownToolbarButton Class](../vs140/CMFCDropDownToolbarButton-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBarButton::OnCalculateSize](../vs140/CMFCToolBarButton--OnCalculateSize.md)