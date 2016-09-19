---
title: "COleClientItem::GetItemState"
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
ms.assetid: 5c814a55-21fb-4be7-968f-2ce05b10c1fc
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleClientItem::GetItemState
Call this function to get the OLE item's current state.  
  
## Syntax  
  
```  
  
UINT GetItemState( ) const;  
```  
  
## Return Value  
 A **COleClientItem::ItemState** enumerated value, which can be one of the following: `emptyState`, **loadedState**, `openState`, `activeState`, `activeUIState`. For information about these states, see the article [Containers: Client-Item States](../vs140/Containers--Client-Item-States.md).  
  
## Remarks  
 To be notified when the OLE item's state changes, use the [OnChange](../vs140/COleClientItem--OnChange.md) member function.  
  
 For more information, see the article [Containers: Client-Item States](../vs140/Containers--Client-Item-States.md).  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleClientItem Class](../vs140/COleClientItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleClientItem::OnChange](../vs140/COleClientItem--OnChange.md)