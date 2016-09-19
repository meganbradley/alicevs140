---
title: "CListCtrl::RedrawItems"
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
ms.assetid: d4670cd1-9eca-46db-b067-5170efa1e134
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::RedrawItems
Forces a list view control to repaint a range of items.  
  
## Syntax  
  
```  
  
      BOOL RedrawItems(  
   int nFirst,  
   int nLast   
);  
```  
  
#### Parameters  
 `nFirst`  
 Index of the first item to be repainted.  
  
 `nLast`  
 Index of the last item to be repainted.  
  
## Return Value  
 Nonzero if successful; otherwise zero.  
  
## Remarks  
 The specified items are not actually repainted until the list view window receives a `WM_PAINT` message. To repaint immediately, call the Windows [UpdateWindow](http://msdn.microsoft.com/library/windows/desktop/dd145167) function after using this function.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListCtrl::DrawItem](../vs140/CListCtrl--DrawItem.md)