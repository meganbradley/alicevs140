---
title: "CMFCToolBarComboBoxButton::CreateCombo"
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
ms.assetid: 9a539674-3e2d-402a-a354-8e7a19bb3d2b
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarComboBoxButton::CreateCombo
Creates a new combo box for the combo box button.  
  
## Syntax  
  
```  
virtual CComboBox* CreateCombo(  
   CWnd* pWndParent,  
   const CRect& rect  
);  
```  
  
#### Parameters  
 [in] `pWndParent`  
 A pointer to the parent window of the button.  
  
 [in] `rect`  
 Bounding rectangle of the combo box.  
  
## Return Value  
 A pointer to the new combo box if the method was successful; otherwise, `NULL`.  
  
## Requirements  
 **Header:** afxtoolbarcomboboxbutton.h  
  
## See Also  
 [CMFCToolBarComboBoxButton Class](../vs140/CMFCToolBarComboBoxButton-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)