---
title: "CMFCColorMenuButton::CMFCColorMenuButton"
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
ms.assetid: 7d786543-dcaa-493c-a000-7a58f379b386
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCColorMenuButton::CMFCColorMenuButton
Constructs a `CMFCColorMenuButton` object.  
  
## Syntax  
  
```  
CMFCColorMenuButton();  
CMFCColorMenuButton(  
   UINT uiCmdID,  
   LPCTSTR lpszText,  
   CPalette* pPalette=NULL   
);  
```  
  
#### Parameters  
 [in] `uiCmdID`  
 A button command ID.  
  
 [in] `lpszText`  
 The button text.  
  
 [in] `pPalette`  
 A pointer to the button's color palette.  
  
## Return Value  
  
## Remarks  
 The first constructor is the default constructor. The object's current color and automatic color are initialized to black (RGB(0, 0, 0)).  
  
 The second constructor initializes the button to the color that corresponds to the specified command ID.  
  
## Requirements  
 **Header:** afxcolormenubutton.h  
  
## See Also  
 [CMFCColorMenuButton Class](../vs140/CMFCColorMenuButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)