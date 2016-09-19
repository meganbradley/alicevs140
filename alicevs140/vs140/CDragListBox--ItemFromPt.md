---
title: "CDragListBox::ItemFromPt"
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
ms.assetid: 31910221-094a-4028-92b2-eb3526405382
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDragListBox::ItemFromPt
Call this function to retrieve the zero-based index of the list box item located at `pt`.  
  
## Syntax  
  
```  
  
      int ItemFromPt(  
   CPoint pt,  
   BOOL bAutoScroll = TRUE   
) const;  
```  
  
#### Parameters  
 `pt`  
 A [CPoint](../vs140/CPoint-Class.md) object containing the coordinates of a point within the list box.  
  
 *bAutoScroll*  
 Nonzero if scrolling is allowed, otherwise 0.  
  
## Return Value  
 Zero-based index of the drag list box item.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CDragListBox Class](../vs140/CDragListBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)