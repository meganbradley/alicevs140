---
title: "CListCtrl::GetOrigin"
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
ms.assetid: 544d7377-a15f-43d4-839a-33781fa59f59
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::GetOrigin
Retrieves the current view origin for a list view control.  
  
## Syntax  
  
```  
  
      BOOL GetOrigin(  
   LPPOINT lpPoint   
) const;  
```  
  
#### Parameters  
 `lpPoint`  
 Address of a [POINT](http://msdn.microsoft.com/library/windows/desktop/dd162805) structure that receives the view origin.  
  
## Return Value  
 Nonzero if successful; otherwise zero. However, if the control is in report view, the return value is always zero.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListCtrl::GetItemPosition](../vs140/CListCtrl--GetItemPosition.md)   
 [CListCtrl::SetItemPosition](../vs140/CListCtrl--SetItemPosition.md)