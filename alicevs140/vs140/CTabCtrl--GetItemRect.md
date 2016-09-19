---
title: "CTabCtrl::GetItemRect"
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
ms.assetid: db48c976-2db6-4c3c-9d84-0c1872d94fba
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTabCtrl::GetItemRect
Retrieves the bounding rectangle for the specified tab in a tab control.  
  
## Syntax  
  
```  
  
      BOOL GetItemRect(  
  int nItem,  
  LPRECT lpRect   
) const;  
```  
  
#### Parameters  
 `nItem`  
 Zero-based index of the tab item.  
  
 `lpRect`  
 Pointer to a [RECT](http://msdn.microsoft.com/library/windows/desktop/dd162897) structure that receives the bounding rectangle of the tab. These coordinates use the viewport's current mapping mode.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Example  
 See the example for [CPropertySheet::GetTabControl](../vs140/CPropertySheet--GetTabControl.md).  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CTabCtrl Class](../vs140/CTabCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTabCtrl::SetItemSize](../vs140/CTabCtrl--SetItemSize.md)   
 [CTabCtrl::AdjustRect](../vs140/CTabCtrl--AdjustRect.md)