---
title: "CMFCToolBarsCustomizeDialog::FillCategoriesComboBox"
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
ms.assetid: 2b40e59d-a51a-49cf-9d52-289a43d28be5
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarsCustomizeDialog::FillCategoriesComboBox
Populates the provided `CComboBox` object with the name of each command category in the **Customize** dialog box.  
  
## Syntax  
  
```  
void FillCategoriesComboBox(  
   CComboBox& wndCategory,  
   BOOL bAddEmpty = TRUE  
) const;  
```  
  
#### Parameters  
 [out] `wndCategory`  
 A reference to the `CComboBox` object to populate.  
  
 [in] `bAddEmpty`  
 A Boolean value that specifies whether to add categories to the combo box that do not have commands. If this parameter is `TRUE`, empty categories are added to the combo box. Otherwise, empty categories are not added.  
  
## Remarks  
 This method is like the [CMFCToolBarsCustomizeDialog::FillCategoriesListBox](../vs140/CMFCToolBarsCustomizeDialog--FillCategoriesListBox.md) method except that this method works with a `CComboBox` object.  
  
 This method does not clear the contents of the `CComboBox` object before populating it. It guarantees that the **All Commands** category is the final item in the combo box.  
  
 You can add new command categories by using the [CMFCToolBarsCustomizeDialog::AddButton](../vs140/CMFCToolBarsCustomizeDialog--AddButton.md) method. You can change the name of an existing category by using the [CMFCToolBarsCustomizeDialog::RenameCategory](../vs140/CMFCToolBarsCustomizeDialog--RenameCategory.md) method.  
  
 The `CMFCToolBarsKeyboardPropertyPage` and `CMFCKeyMapDialog` classes use this method to categorize keyboard mappings.  
  
## Requirements  
 **Header:** afxtoolbarscustomizedialog.h  
  
## See Also  
 [CMFCToolBarsCustomizeDialog Class](../vs140/CMFCToolBarsCustomizeDialog-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CComboBox Class](../vs140/CComboBox-Class.md)   
 [CMFCToolBarsCustomizeDialog::FillCategoriesListBox](../vs140/CMFCToolBarsCustomizeDialog--FillCategoriesListBox.md)   
 [CMFCToolBarsCustomizeDialog::AddButton](../vs140/CMFCToolBarsCustomizeDialog--AddButton.md)   
 [CMFCToolBarsCustomizeDialog::RenameCategory](../vs140/CMFCToolBarsCustomizeDialog--RenameCategory.md)   
 [CMFCKeyMapDialog Class](../vs140/CMFCKeyMapDialog-Class.md)