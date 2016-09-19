---
title: "CListCtrl::Scroll"
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
ms.assetid: 9f2f0bfd-1068-43bd-87bc-6be7e466a1ce
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::Scroll
Scrolls the content of a list view control.  
  
## Syntax  
  
```  
  
      BOOL Scroll(  
   CSize size   
);  
```  
  
#### Parameters  
 `size`  
 A `CSize` object specifying the amount of horizontal and vertical scrolling, in pixels. The **y** member of `size` is divided by the height, in pixels, of the list view control's line, and the control is scrolled by the resulting number of lines.  
  
## Return Value  
 Nonzero if successful; otherwise zero.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListCtrl::EnsureVisible](../vs140/CListCtrl--EnsureVisible.md)