---
title: "CMFCToolBarsCustomizeDialog::FillCategoriesListBox"
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
ms.assetid: 7d2a476c-fbe2-4e68-8e31-7c397a9fc616
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarsCustomizeDialog::FillCategoriesListBox
Populates the provided `CListBox` object with the name of each command category in the **Customize** dialog box.  
  
## Syntax  
  
```  
void FillCategoriesListBox(  
   CListBox& wndCategory,  
   BOOL bAddEmpty = TRUE  
) const;  
```  
  
#### Parameters  
 [out] `wndCategory`  
 A reference to the `CListBox` object to populate.  
  
 [in] `bAddEmpty`  
 A Boolean value that specifies whether to add categories to the list box that do not have commands. If this parameter is `TRUE`, empty categories are added to the list box. Otherwise, empty categories are not added.  
  
## Remarks  
 This method is like the [CMFCToolBarsCustomizeDialog::FillCategoriesComboBox](../vs140/CMFCToolBarsCustomizeDialog--FillCategoriesComboBox.md) method except that this method works with a `CListBox` object.  
  
 This method does not clear the contents of the `CListBox` object before populating it. It guarantees that the **All Commands** category is the final item in the list box.  
  
 You can add new command categories by using the [CMFCToolBarsCustomizeDialog::AddButton](../vs140/CMFCToolBarsCustomizeDialog--AddButton.md) method. You can change the name of an existing category by using the [CMFCToolBarsCustomizeDialog::RenameCategory](../vs140/CMFCToolBarsCustomizeDialog--RenameCategory.md) method.  
  
 The `CMFCToolBarsCommandsPropertyPage` class uses this method to show the list of commands that is associated with each command category.  
  
## Requirements  
 **Header:** afxtoolbarscustomizedialog.h  
  
## See Also  
 [CMFCToolBarsCustomizeDialog Class](../vs140/CMFCToolBarsCustomizeDialog-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CListBox Class](../vs140/CListBox-Class.md)   
 [CMFCToolBarsCustomizeDialog::FillCategoriesComboBox](../vs140/CMFCToolBarsCustomizeDialog--FillCategoriesComboBox.md)   
 [CMFCToolBarsCustomizeDialog::AddButton](../vs140/CMFCToolBarsCustomizeDialog--AddButton.md)   
 [CMFCToolBarsCustomizeDialog::RenameCategory](../vs140/CMFCToolBarsCustomizeDialog--RenameCategory.md)