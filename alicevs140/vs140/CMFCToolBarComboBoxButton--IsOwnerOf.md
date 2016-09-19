---
title: "CMFCToolBarComboBoxButton::IsOwnerOf"
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
ms.assetid: 29f7bf41-976d-4f53-ac68-2398f1cbb9c8
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarComboBoxButton::IsOwnerOf
Indicates whether the specified handle is associated with the combo box button, or one of its children.  
  
## Syntax  
  
```  
virtual BOOL IsOwnerOf(  
   HWND hwnd  
);  
```  
  
#### Parameters  
 [in] `hwnd`  
 A window handle.  
  
## Return Value  
 `TRUE` if the handle is assocated with the combo box button, or one of its children; otherwise, `FALSE`.  
  
## Requirements  
 **Header:** afxtoolbarcomboboxbutton.h  
  
## See Also  
 [CMFCToolBarComboBoxButton Class](../vs140/CMFCToolBarComboBoxButton-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)