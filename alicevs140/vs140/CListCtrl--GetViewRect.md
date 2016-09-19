---
title: "CListCtrl::GetViewRect"
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
ms.assetid: c786f5b7-01ca-480d-bacc-5b59356a12ea
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::GetViewRect
Retrieves the bounding rectangle of all items in the list view control.  
  
## Syntax  
  
```  
  
      BOOL GetViewRect(  
   LPRECT lpRect   
) const;  
```  
  
#### Parameters  
 `lpRect`  
 Address of a [RECT](http://msdn.microsoft.com/library/windows/desktop/dd162897) structure.  
  
## Return Value  
 Nonzero if successful; otherwise zero.  
  
## Remarks  
 The list view must be in icon view or small icon view.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListCtrl::GetTopIndex](../vs140/CListCtrl--GetTopIndex.md)