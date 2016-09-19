---
title: "CMFCDropDownFrame::GetParentPopupMenu"
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
ms.assetid: 7ff98ecd-e7fa-47be-9761-b8ccd4307050
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCDropDownFrame::GetParentPopupMenu
Retrieves the parent pop-up menu of the drop-down frame.  
  
## Syntax  
  
```  
CMFCDropDownFrame* GetParentPopupMenu() const;  
```  
  
## Return Value  
 A pointer to the parent drop-down menu of the drop-down frame, or `NULL` if the frame has no parent.  
  
## Remarks  
 This method retrieves the parent menu from the parent button. This method returns `NULL` if the drop-down frame has no parent button or the parent button has no parent menu.  
  
## Requirements  
 **Header:** afxdropdowntoolbar.h  
  
## See Also  
 [CMFCDropDownFrame Class](../vs140/CMFCDropDownFrame-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCMenuBar Class](../vs140/CMFCMenuBar-Class.md)