---
title: "CMFCToolBarComboBoxButton::CMFCToolBarComboBoxButton"
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
ms.assetid: 3c296d8f-8fe3-48a2-8fa3-4b032805fac3
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarComboBoxButton::CMFCToolBarComboBoxButton
Constructs a [CMFCToolBarComboBoxButton Class](../vs140/CMFCToolBarComboBoxButton-Class.md) object.  
  
## Syntax  
  
```  
CMFCToolBarComboBoxButton(  
   UINT uiID,  
   int iImage,  
   DWORD dwStyle=CBS_DROPDOWNLIST,  
   int iWidth=0   
);  
```  
  
#### Parameters  
 [in] `uiID`  
 The command ID of the new button.  
  
 [in] `iImage`  
 The image index of the image associated with the new button.  
  
 [in] `dwStyle`  
 The style of the new button.  
  
 [in] `iWidth`  
 The width, in pixels, of the new button.  
  
## Remarks  
 The default width is 150 pixels.  
  
 For a list of toolbar button styles see [ToolBar Control Styles](../vs140/ToolBar-Control-Styles.md)  
  
## Requirements  
 **Header:** afxtoolbarcomboboxbutton.h  
  
## See Also  
 [CMFCToolBarComboBoxButton Class](../vs140/CMFCToolBarComboBoxButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)