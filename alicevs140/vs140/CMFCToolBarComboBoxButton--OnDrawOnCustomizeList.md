---
title: "CMFCToolBarComboBoxButton::OnDrawOnCustomizeList"
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
ms.assetid: e04d98a1-d57c-40d4-84bd-42e29d749058
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarComboBoxButton::OnDrawOnCustomizeList
Called by the framework to draw the combo box button in the **Commands** pane of the **Customize** dialog box.  
  
## Syntax  
  
```  
virtual int OnDrawOnCustomizeList(  
   CDC* pDC,  
   const CRect& rect,  
   BOOL bSelected  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 The device context that displays the combo box button.  
  
 [in] `rect`  
 The bounding rectangle of the combo box button.  
  
 [in] `bSelected`  
 `TRUE` if the combo box button is selected; otherwise, `FALSE`.  
  
## Return Value  
 The width, in pixels, of the combo box button.  
  
## Requirements  
 **Header:** afxtoolbarcomboboxbutton.h  
  
## See Also  
 [CMFCToolBarComboBoxButton Class](../vs140/CMFCToolBarComboBoxButton-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)