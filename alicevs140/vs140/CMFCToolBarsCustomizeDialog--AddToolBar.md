---
title: "CMFCToolBarsCustomizeDialog::AddToolBar"
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
ms.assetid: cb2c9879-bc43-4d08-9aac-4a153eaa8e2e
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarsCustomizeDialog::AddToolBar
Loads a toolbar from the resources. Then, for each command in the menu calls the [CMFCToolBarsCustomizeDialog::AddButton](../vs140/CMFCToolBarsCustomizeDialog--AddButton.md) method to insert a button in the list of commands on the **Commands** page under the specified category.  
  
## Syntax  
  
```  
BOOL AddToolBar(  
   UINT uiCategoryId,  
   UINT uiToolbarResId   
);  
BOOL AddToolBar(  
   LPCTSTR lpszCategory,  
   UINT uiToolbarResId   
);  
```  
  
#### Parameters  
 [in] `uiCategoryId`  
 Specifies the resource ID of the category to add the toolbar to.  
  
 [in] `uiToolbarResId`  
 Specifies the resource ID of a toolbar whose commands are inserted into the list of commands.  
  
 [in] `lpszCategory`  
 Specifies the name of the category to which to add the toolbar.  
  
## Return Value  
 `TRUE` if the method is successful; otherwise `FALSE`.  
  
## Example  
 The following example demonstrates how to use the `AddToolBar` method in the `CMFCToolBarsCustomizeDialog` class. This code snippet is part of the [Word Pad sample](../vs140/Visual-C---Samples.md).  
  
 [!CODE [NVC_MFC_WordPad#11](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_WordPad#11)]  
  
## Remarks  
 The control that is used to represent each command is a [CMFCToolBarButton](../vs140/CMFCToolBarButton-Class.md) object. After you add the toolbar, you can replace the button with a control of a derived type by calling [CMFCToolBarsCustomizeDialog::ReplaceButton](../vs140/CMFCToolBarsCustomizeDialog--ReplaceButton.md).  
  
## Requirements  
 **Header:** afxToolBarsCustomizeDialog.h  
  
## See Also  
 [CMFCToolBarsCustomizeDialog Class](../vs140/CMFCToolBarsCustomizeDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)