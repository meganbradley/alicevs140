---
title: "CMFCToolBarComboBoxButton::CreateEdit"
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
ms.assetid: 9d679b7d-dd31-4a2a-bcff-5cdbafb7d9a5
caps.latest.revision: 22
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarComboBoxButton::CreateEdit
Creates a new edit box for the combo box button.  
  
## Syntax  
  
```  
virtual CMFCToolBarComboBoxEdit* CreateEdit(  
   CWnd* pWndParent,  
   const CRect& rect,  
   DWORD dwEditStyle   
);  
```  
  
#### Parameters  
 [in] `pWndParent`  
 A pointer to the parent window of the button.  
  
 [in] `rect`  
 Bounding rectangle of the new edit box.  
  
 [in] `dwEditStyle`  
 Control style of the new edit box.  
  
## Return Value  
 A pointer to the new edit box if the method was successful; otherwise, `NULL`.  
  
## Remarks  
 The framework calls this method when it creates a new edit box for a combo box button. Override this method to change how [CMFCToolBarComboBoxEdit](../vs140/CMFCToolBarComboBoxEdit-Class.md) is created.  
  
## Requirements  
 **Header:** afxtoolbarcomboboxbutton.h  
  
## See Also  
 [CMFCToolBarComboBoxButton Class](../vs140/CMFCToolBarComboBoxButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBarComboBoxEdit Class](../vs140/CMFCToolBarComboBoxEdit-Class.md)