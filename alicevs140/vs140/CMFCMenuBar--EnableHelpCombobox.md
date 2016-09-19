---
title: "CMFCMenuBar::EnableHelpCombobox"
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
ms.assetid: 9d940546-a07b-4b28-8641-a98b30f8adea
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCMenuBar::EnableHelpCombobox
Enables a **Help** combo box that is located on the right side of the menu bar.  
  
## Syntax  
  
```  
void EnableHelpCombobox(  
   UINT uiID,  
   LPCTSTR lpszPrompt = NULL,  
   int nComboBoxWidth = 150   
);  
```  
  
#### Parameters  
 [in] `uiID`  
 The command ID for the button of the **Help** combo box.  
  
 [in] `lpszPrompt`  
 A string that contains the text that the framework displays in the combo box if it is empty and not active. For example, "Enter the text here".  
  
 [in] `nComboBoxWidth`  
 The width of the button for the combo box in pixels.  
  
## Remarks  
 The **Help** combo box resembles the **Help** combo box in the menu bar of [!INCLUDE[ofprword](../vs140/includes/ofprword_md.md)].  
  
 When you call this method with `uiID` set to 0, this method hides the combo box. Otherwise, this method displays the combo box automatically on the right side of your menu bar. After you call this method, call [CMFCMenuBar::GetHelpCombobox](../vs140/CMFCMenuBar--GetHelpCombobox.md) to obtain a pointer to the inserted [CMFCToolBarComboBoxButton](../vs140/CMFCToolBarComboBoxButton-Class.md) object.  
  
## Requirements  
 **Header:** afxmenubar.h  
  
## See Also  
 [CMFCMenuBar Class](../vs140/CMFCMenuBar-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)