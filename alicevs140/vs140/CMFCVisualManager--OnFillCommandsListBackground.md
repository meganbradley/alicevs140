---
title: "CMFCVisualManager::OnFillCommandsListBackground"
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
ms.assetid: f9013b09-4fc5-4403-b1d4-6d1e0733a0d3
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManager::OnFillCommandsListBackground
The framework calls this method when it fills the background of a toolbar button that belongs to a command list. This command list is part of the customization dialog.  
  
## Syntax  
  
```  
virtual COLORREF OnFillCommandsListBackground(  
   CDC* pDC,  
   CRect rect,  
   BOOL bIsSelected = FALSE  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context.  
  
 [in] `rect`  
 A rectangle that specifies the boundaries of the button.  
  
 [in] `bIsSelected`  
 A Boolean parameter that indicates whether the button is selected.  
  
## Return Value  
 The text color for the toolbar button.  
  
## Remarks  
 For more information about the customization list, see [CMFCToolBarButton::OnDrawOnCustomizeList](../vs140/CMFCToolBarButton--OnDrawOnCustomizeList.md). The default implementation for this method fills the background based on the color scheme of the currently selected skin.  
  
## Requirements  
 **Header:** afxvisualmanager.h  
  
## See Also  
 [CMFCVisualManager Class](../vs140/CMFCVisualManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)