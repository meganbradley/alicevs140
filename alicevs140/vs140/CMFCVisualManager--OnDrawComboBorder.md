---
title: "CMFCVisualManager::OnDrawComboBorder"
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
ms.assetid: bee7fce8-7b84-4f4f-a8ab-89d5cf261ae4
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManager::OnDrawComboBorder
The framework calls this method when it draws the border around an instance of the [CMFCToolBarComboBoxButton Class](../vs140/CMFCToolBarComboBoxButton-Class.md).  
  
## Syntax  
  
```  
virtual void OnDrawComboBorder(  
   CDC* pDC,  
   CRect rect,  
   BOOL bDisabled,  
   BOOL bIsDropped,  
   BOOL bIsHighlighted,  
   CMFCToolBarComboBoxButton* pButton   
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to the device context of a combo box button.  
  
 [in] `rect`  
 A rectangle that specifies the boundaries of the combo box button.  
  
 [in] `bDisabled`  
 A Boolean parameter that indicates whether the combo box button is unavailable.  
  
 [in] `bIsDropped`  
 A Boolean parameter that indicates whether the combo box is dropped down.  
  
 [in] `bIsHighlighted`  
 A Boolean parameter that indicates whether the combo box button is highlighted.  
  
 [in] `pButton`  
 A pointer to a `CMFCToolBarComboBoxButton` object. The framework draws this combo box button.  
  
## Remarks  
 Override this method in your derived visual manager to customize the appearance of the border of the combo box.  
  
## Requirements  
 **Header:** afxvisualmanager.h  
  
## See Also  
 [CMFCVisualManager Class](../vs140/CMFCVisualManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBarComboBoxButton Class](../vs140/CMFCToolBarComboBoxButton-Class.md)