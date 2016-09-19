---
title: "CMFCDropDownToolbarButton::CMFCDropDownToolbarButton"
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
ms.assetid: bd35b044-b003-4e4e-b4f1-5a1231612d30
caps.latest.revision: 19
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCDropDownToolbarButton::CMFCDropDownToolbarButton
Constructs a `CMFCDropDownToolbarButton` object.  
  
## Syntax  
  
```  
CMFCDropDownToolbarButton();  
CMFCDropDownToolbarButton(  
   LPCTSTR lpszName,  
   CMFCDropDownToolBar* pToolBar   
);  
```  
  
#### Parameters  
 [in] `lpszName`  
 The default text of the button.  
  
 [in] `pToolBar`  
 A pointer to the `CMFCDropDownToolBar` object that is displayed when the user presses the button.  
  
## Remarks  
 The second overload of the constructor copies to the drop-down button the first button from the toolbar that `pToolBar` specifies.  
  
 Typically, a drop-down toolbar button uses the text from the most recently used button in the toolbar that `pToolBar` specifies. It uses the text specified by `lpszName` when the button is converted to a menu button or is displayed in the **Commands** tab of the **Customize** dialog box. For more information about the **Customize** dialog box, see [CMFCToolBarsCustomizeDialog](../vs140/CMFCToolBarsCustomizeDialog-Class.md).  
  
## Example  
 The following example demonstrates how to construct an object of the `CMFCDropDownToolbarButton` class. This code snippet is part of the [Visual Studio Demo sample](../vs140/Visual-C---Samples.md).  
  
 [!CODE [NVC_MFC_VisualStudioDemo#31](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_VisualStudioDemo#31)]  
  
## Requirements  
 **Header:** afxdropdowntoolbar.h  
  
## See Also  
 [CMFCDropDownToolbarButton Class](../vs140/CMFCDropDownToolbarButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCDropDownToolBar Class](../vs140/CMFCDropDownToolBar-Class.md)   
 [CMFCToolBarsCustomizeDialog](../vs140/CMFCToolBarsCustomizeDialog-Class.md)