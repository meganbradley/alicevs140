---
title: "CMFCToolBar::SetTwoRowsWithSibling"
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
ms.assetid: 264d889b-0c45-46d4-8800-a986e84e814a
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::SetTwoRowsWithSibling
Positions the toolbar and its sibling on separate rows.  
  
## Syntax  
  
```  
void SetTwoRowsWithSibling();  
```  
  
## Remarks  
 The framework calls this method when the user clicks the **Show Buttons on Two Rows** button.  
  
 Call the [CMFCToolBar::SetSiblingToolBar](../vs140/CMFCToolBar--SetSiblingToolBar.md) method to enable the **Show Buttons on One Row** or **Show Buttons on Two Rows** buttons. If you call [CMFCToolBar::SetSiblingToolBar](../vs140/CMFCToolBar--SetSiblingToolBar.md) for this toolbar, the sibling toolbar is moved to a separate row. Otherwise, this toolbar is moved to a separate row.  
  
 The framework calls the [CMFCToolBar::SetOneRowWithSibling](../vs140/CMFCToolBar--SetOneRowWithSibling.md) method when the user clicks the **Show Buttons on One Row** button.  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBar::SetSiblingToolBar](../vs140/CMFCToolBar--SetSiblingToolBar.md)   
 [CMFCToolBar::SetOneRowWithSibling](../vs140/CMFCToolBar--SetOneRowWithSibling.md)