---
title: "COleClientItem::IsInPlaceActive"
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
ms.assetid: b4621409-27e0-4dd8-80e8-c4350fd05b5f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleClientItem::IsInPlaceActive
Call this function to see whether the OLE item is in-place active.  
  
## Syntax  
  
```  
  
BOOL IsInPlaceActive( ) const;  
```  
  
## Return Value  
 Nonzero if the OLE item is in-place active; otherwise 0.  
  
## Remarks  
 It is common to execute different logic depending on whether the item is being edited in place. The function checks whether the current item state is equal to either the `activeState` or the `activeUIState`.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleClientItem Class](../vs140/COleClientItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleClientItem::GetItemState](../vs140/COleClientItem--GetItemState.md)