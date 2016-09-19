---
title: "CMFCVisualManager::OnDrawEditBorder"
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
ms.assetid: b202b907-6596-4512-b2e7-757fb384eb97
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManager::OnDrawEditBorder
The framework calls this method when it draws the border around an instance of the [CMFCToolBarEditBoxButton Class](../vs140/CMFCToolBarEditBoxButton-Class.md).  
  
## Syntax  
  
```  
virtual void OnDrawEditBorder(  
   CDC* pDC,  
   CRect rect,  
   BOOL bDisabled,  
   BOOL bIsHighlighted,  
   CMFCToolBarEditBoxButton* pButton   
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context.  
  
 [in] `rect`  
 A rectangle that specifies the boundaries of the `CMFCToolBarEditBoxButton` object.  
  
 [in] `bDisabled`  
 A Boolean parameter that indicates whether the button is unavailable.  
  
 [in] `bIsHighlighted`  
 A Boolean parameter that indicates whether the button is highlighted.  
  
 [in] `pButton`  
 A pointer to a `CMFCToolBarEditBoxButton` object. The framework draws the border of this edit box button.  
  
## Remarks  
 Override this method in a derived visual manager to customize the border of a `CMFCToolBarEditBoxButton` object.  
  
## Requirements  
 **Header:** afxvisualmanager.h  
  
## See Also  
 [CMFCVisualManager Class](../vs140/CMFCVisualManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBarEditBoxButton Class](../vs140/CMFCToolBarEditBoxButton-Class.md)