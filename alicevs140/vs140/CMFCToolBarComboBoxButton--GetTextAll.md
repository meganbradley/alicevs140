---
title: "CMFCToolBarComboBoxButton::GetTextAll"
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
ms.assetid: 83b2a158-fe15-42de-b07f-6b70d013f02a
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarComboBoxButton::GetTextAll
Gets the text in the edit box of a combo box button that has a specified command ID.  
  
## Syntax  
  
```  
static LPCTSTR GetTextAll(  
   UINT uiCmd   
);  
```  
  
#### Parameters  
 [in] `uiCmd`  
 The command ID of a specific combo box button.  
  
## Return Value  
 The text in the edit box if the method was successful; otherwise, `NULL`.  
  
## Remarks  
  
## Requirements  
 **Header:** afxtoolbarcomboboxbutton.h  
  
## See Also  
 [CMFCToolBarComboBoxButton Class](../vs140/CMFCToolBarComboBoxButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)