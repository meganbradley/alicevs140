---
title: "CMFCToolBarComboBoxButton::GetByCmd"
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
ms.assetid: 10d1ed54-ca34-4f36-8ad1-39db9d92b1b7
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarComboBoxButton::GetByCmd
Gets a pointer to the combo box button that has a specified command ID.  
  
## Syntax  
  
```  
static CMFCToolBarComboBoxButton* GetByCmd(  
   UINT uiCmd,  
   BOOL bIsFocus=FALSE   
);  
```  
  
#### Parameters  
 [in] `uiCmd`  
 The command ID of a combo box button.  
  
 [in] `bIsFocus`  
 `TRUE` to search only focused buttons; `FALSE` to search all buttons.  
  
## Return Value  
 A pointer to a combo box button; or `NULL` if the button is not found.  
  
## Remarks  
  
## Requirements  
 **Header:** afxtoolbarcomboboxbutton.h  
  
## See Also  
 [CMFCToolBarComboBoxButton Class](../vs140/CMFCToolBarComboBoxButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)