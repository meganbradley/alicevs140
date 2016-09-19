---
title: "CMFCMenuBar::GetHelpCombobox"
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
ms.assetid: 271238fa-9f93-4e49-948c-3409d99a9899
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCMenuBar::GetHelpCombobox
Returns a pointer to the **Help** combo box.  
  
## Syntax  
  
```  
CMFCToolBarComboBoxButton* GetHelpCombobox();  
```  
  
## Return Value  
 A pointer to the **Help** combo box. `NULL` if the **Help** combo box is hidden or not enabled.  
  
## Remarks  
 The **Help** combo box is located on the right side of the menu bar. Call the method [CMFCMenuBar::EnableHelpCombobox](../vs140/CMFCMenuBar--EnableHelpCombobox.md) to enable this combo box.  
  
## Requirements  
 **Header:** afxmenubar.h  
  
## See Also  
 [CMFCMenuBar Class](../vs140/CMFCMenuBar-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCMenuBar::EnableHelpCombobox](../vs140/CMFCMenuBar--EnableHelpCombobox.md)