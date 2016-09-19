---
title: "CMFCToolBarComboBoxButton::OnCalculateSize"
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
ms.assetid: ed82899a-0979-4928-8dcd-bd1949197b3f
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarComboBoxButton::OnCalculateSize
Called by the framework to calculate the size of the button.  
  
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
 The device context that displays the combo box button.  
  
 [in] `sizeDefault`  
 The default size of the combo box button.  
  
 [in] `bHorz`  
 The dock state of the parent toolbar. `TRUE` when the toolbar is docked horizontally and `FALSE` when the toolbar is docked vertically.  
  
## Return Value  
 A `SIZE` structure that contains the dimensions of the combo box button, in pixels.  
  
## Requirements  
 **Header:** afxtoolbarcomboboxbutton.h  
  
## See Also  
 [CMFCToolBarComboBoxButton Class](../vs140/CMFCToolBarComboBoxButton-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)