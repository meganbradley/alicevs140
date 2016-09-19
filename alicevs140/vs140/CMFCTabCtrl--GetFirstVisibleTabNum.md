---
title: "CMFCTabCtrl::GetFirstVisibleTabNum"
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
ms.assetid: fdd99cbb-4e64-493d-b336-0ec70afe4cc9
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCTabCtrl::GetFirstVisibleTabNum
Retrieves the index of the first tab that is visible in the current tab control.  
  
## Syntax  
  
```  
virtual int GetFirstVisibleTabNum() const;  
```  
  
## Return Value  
 The zero-based index of a tab in the tab control.  
  
## Remarks  
 Use this method only when the tab control is displayed in the style of Microsoft OneNote. Use the [CMFCTabCtrl::IsOneNoteStyle](../vs140/CMFCTabCtrl--IsOneNoteStyle.md) method to determine the style.  
  
## Requirements  
 **Header:** afxtabctrl.h  
  
## See Also  
 [CMFCTabCtrl Class](../vs140/CMFCTabCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCTabCtrl::IsOneNoteStyle](../vs140/CMFCTabCtrl--IsOneNoteStyle.md)