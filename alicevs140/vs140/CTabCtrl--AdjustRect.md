---
title: "CTabCtrl::AdjustRect"
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
ms.assetid: 84abe214-ff93-40bb-9dcb-b5038582136a
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTabCtrl::AdjustRect
Calculates a tab control's display area given a window rectangle, or calculates the window rectangle that would correspond to a given display area.  
  
## Syntax  
  
```  
  
      void AdjustRect(  
  BOOL bLarger,  
  LPRECT lpRect   
);  
```  
  
#### Parameters  
 `bLarger`  
 Indicates which operation to perform. If this parameter is **TRUE**, `lpRect` specifies a display rectangle and receives the corresponding window rectangle. If this parameter is **FALSE**, `lpRect` specifies a window rectangle and receives the corresponding display rectangle.  
  
 `lpRect`  
 Pointer to a [RECT](http://msdn.microsoft.com/library/windows/desktop/dd162897) structure that specifies the given rectangle and receives the calculated rectangle.  
  
## Example  
 [!CODE [NVC_MFC_CTabCtrl#1](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CTabCtrl#1)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CTabCtrl Class](../vs140/CTabCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTabCtrl::SetItemSize](../vs140/CTabCtrl--SetItemSize.md)   
 [CTabCtrl::GetItemRect](../vs140/CTabCtrl--GetItemRect.md)   
 [CTabCtrl::AdjustRect](../vs140/CTabCtrl--AdjustRect.md)