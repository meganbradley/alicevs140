---
title: "CMFCToolBar::IsOneRowWithSibling"
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
ms.assetid: 63bc2fce-a22b-4a61-8ec7-afedabeea80b
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::IsOneRowWithSibling
Determines whether the toolbar and its sibling toolbar are positioned on the same row.  
  
## Syntax  
  
```  
BOOL IsOneRowWithSibling();  
```  
  
## Return Value  
 `TRUE` if the toolbar and its sibling are positioned on the same row; otherwise `FALSE`.  
  
## Remarks  
 The [CMFCCustomizeButton::CreatePopupMenu](assetId:///e501083e-f78e-4d8d-900c-40bd6e2bb7f8) method calls this method to determine how to show the **Customize** pop-up menu. If this method returns `TRUE`, the framework displays the **Show Buttons on One Row** button. Otherwise, the framework displays the **Show Buttons on Two Rows** button.  
  
 You typically do not have to use this method. To enable the **Show Buttons on One Row** or **Show Buttons on Two Rows** buttons, call [CMFCToolBar::SetSiblingToolBar](../vs140/CMFCToolBar--SetSiblingToolBar.md).  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCCustomizeButton::CreatePopupMenu](assetId:///e501083e-f78e-4d8d-900c-40bd6e2bb7f8)   
 [CMFCToolBar::SetSiblingToolBar](../vs140/CMFCToolBar--SetSiblingToolBar.md)