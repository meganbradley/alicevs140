---
title: "CMFCDropDownFrame::GetParentMenuBar"
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
ms.assetid: a73beab2-5250-445a-ac26-4f8bc90fa82c
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCDropDownFrame::GetParentMenuBar
Retrieves the parent menu bar of the drop-down frame.  
  
## Syntax  
  
```  
CMFCMenuBar* GetParentMenuBar() const;  
```  
  
## Return Value  
 A pointer to the parent menu bar of the drop-down frame, or `NULL` if the frame has no parent.  
  
## Remarks  
 This method retrieves the parent menu bar from the parent button. This method returns `NULL` if the drop-down frame has no parent button or the parent button has no parent menu bar.  
  
## Requirements  
 **Header:** afxdropdowntoolbar.h  
  
## See Also  
 [CMFCDropDownFrame Class](../vs140/CMFCDropDownFrame-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCMenuBar Class](../vs140/CMFCMenuBar-Class.md)