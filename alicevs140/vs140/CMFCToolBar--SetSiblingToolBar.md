---
title: "CMFCToolBar::SetSiblingToolBar"
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
ms.assetid: 7ba869fb-f153-45cf-8505-c17becfa3743
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::SetSiblingToolBar
Specifies the sibling of the toolbar.  
  
## Syntax  
  
```  
void SetSiblingToolBar(  
   CMFCToolBar* pBrotherToolbar  
);  
```  
  
#### Parameters  
 [in] `pBrotherToolbar`  
 A pointer to the sibling toolbar.  
  
## Remarks  
 This method enables the **Show Buttons on One Row** or **Show Buttons on Two Rows** buttons that are shown when the user displays the **Customize** pop-up menu. Call this method when you want to enable the user to specify whether related toolbars appear on the same row or on different rows.  
  
 Call this method after you enable the **Customize** button that appears on the toolbar. To enable the **Customize** button, call the [CMFCToolBar::EnableCustomizeButton](../vs140/CMFCToolBar--EnableCustomizeButton.md) method.  
  
 To retrieve the sibling of a toolbar, call [CMFCToolBar::GetSiblingToolBar](../vs140/CMFCToolBar--GetSiblingToolBar.md).  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBar::EnableCustomizeButton](../vs140/CMFCToolBar--EnableCustomizeButton.md)   
 [CMFCToolBar::GetSiblingToolBar](../vs140/CMFCToolBar--GetSiblingToolBar.md)