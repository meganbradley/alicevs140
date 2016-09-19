---
title: "CMFCVisualManager::OnDrawComboDropButton"
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
ms.assetid: bca7e337-1ca4-42dc-bdea-bbe0754cc958
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManager::OnDrawComboDropButton
The framework calls this method when it draws the drop button of a [CMFCToolBarComboBoxButton](../vs140/CMFCToolBarComboBoxButton-Class.md).  
  
## Syntax  
  
```  
virtual void OnDrawComboDropButton(  
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
 A pointer to a device context.  
  
 [in] `rect`  
 A rectangle that specifies the boundaries of the drop button.  
  
 [in] `bDisabled`  
 A Boolean parameter that indicates whether the drop button is unavailable.  
  
 [in] `bIsDropped`  
 A Boolean parameter that indicates whether the combo box is dropped down.  
  
 [in] `bIsHighlighted`  
 A Boolean parameter that indicates whether the drop button is highlighted.  
  
 [in] `pButton`  
 A pointer to a `CMFCToolBarComboBoxButton` object. The framework draws the drop button for this combo box button.  
  
## Remarks  
 Override this method in your derived visual manager to customize the appearance of the drop button of a combo box button.  
  
## Requirements  
 **Header:** afxvisualmanager.h  
  
## See Also  
 [CMFCVisualManager Class](../vs140/CMFCVisualManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBarComboBoxButton Class](../vs140/CMFCToolBarComboBoxButton-Class.md)