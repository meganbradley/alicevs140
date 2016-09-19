---
title: "CListCtrl::InsertMarkHitTest"
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
ms.assetid: 327a2a95-a193-4fe7-ada4-a5d9877bf13d
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListCtrl::InsertMarkHitTest
Retrieves the insertion point closest to a specified point.  
  
## Syntax  
  
```  
  
      int InsertMarkHitTest(  
   LPPOINT pPoint,  
   LPLVINSERTMARK lvim   
) const;  
```  
  
#### Parameters  
 `pPoint`  
 A pointer to a [POINT](http://msdn.microsoft.com/library/windows/desktop/dd162805) structure that contains the hit test coordinates, relative to the client area of the list control.  
  
 `lvim`  
 A pointer to an [LVINSERTMARK](http://msdn.microsoft.com/library/windows/desktop/bb774758) structure that specifies the insertion point closest to the coordinates defined by the point parameter.  
  
## Return Value  
 The insertion point closest to the specified point.  
  
## Remarks  
 This member function emulates the functionality of the [LVM_INSERTMARKHITTEST](http://msdn.microsoft.com/library/windows/desktop/bb761131) message, as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CListCtrl Class](../vs140/CListCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListCtrl::GetInsertMark](../vs140/CListCtrl--GetInsertMark.md)   
 [CListCtrl::SetInsertMark](../vs140/CListCtrl--SetInsertMark.md)