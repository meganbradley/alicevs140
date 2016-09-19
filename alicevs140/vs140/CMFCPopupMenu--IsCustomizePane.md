---
title: "CMFCPopupMenu::IsCustomizePane"
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
ms.assetid: 19699577-8759-4a1d-a36f-610dd3ae51ba
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPopupMenu::IsCustomizePane
Indicates whether the pop-up menu is functioning as a **QuickCustomizePane**.  
  
## Syntax  
  
```  
BOOL IsCustomizePane();  
```  
  
## Return Value  
 `TRUE` if the pop-up is a **QuckCustomizePane**; otherwise `FALSE`.  
  
## Remarks  
 Use the **QuickCustomizePane** to enable the user to directly customize the pop-up menu. The **QuickCustomizePane** is a [CMFCPopupMenu](../vs140/CMFCPopupMenu-Class.md) that appears when the user clicks on a toolbar button to edit it directly.  
  
 Your application should call this method during [CMDIFrameWndEx::OnShowCustomizePane](../vs140/CMDIFrameWndEx--OnShowCustomizePane.md).  
  
## Requirements  
 **Header:** afxpopupmenu.h  
  
## See Also  
 [CMFCPopupMenu Class](../vs140/CMFCPopupMenu-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMDIFrameWndEx::OnShowCustomizePane](../vs140/CMDIFrameWndEx--OnShowCustomizePane.md)