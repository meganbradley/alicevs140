---
title: "CMFCToolBar::SetOneRowWithSibling"
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
ms.assetid: 81459d59-5e0d-4e8d-9030-57fd7db945b3
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::SetOneRowWithSibling
Positions the toolbar and its sibling on the same row.  
  
## Syntax  
  
```  
void SetOneRowWithSibling();  
```  
  
## Remarks  
 The framework calls this method when the user clicks the **Show Buttons on One Row** button.  
  
 Call the [CMFCToolBar::SetSiblingToolBar](../vs140/CMFCToolBar--SetSiblingToolBar.md) method to enable the **Show Buttons on One Row** or **Show Buttons on Two Rows** buttons. If you call [CMFCToolBar::SetSiblingToolBar](../vs140/CMFCToolBar--SetSiblingToolBar.md) for this toolbar, the sibling toolbar is moved to the row of this toolbar. Otherwise, this toolbar is moved to the row of the sibling.  
  
 The framework calls the [CMFCToolBar::SetTwoRowsWithSibling](../vs140/CMFCToolBar--SetTwoRowsWithSibling.md) method when the user clicks the **Show Buttons on Two Rows** button.  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBar::SetSiblingToolBar](../vs140/CMFCToolBar--SetSiblingToolBar.md)   
 [CMFCToolBar::SetTwoRowsWithSibling](../vs140/CMFCToolBar--SetTwoRowsWithSibling.md)