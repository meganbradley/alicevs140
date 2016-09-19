---
title: "COleServerItem::IsLinkedItem"
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
ms.assetid: 1abee630-f5a8-4349-95be-f5a262e5e78b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleServerItem::IsLinkedItem
Call this function to see if the OLE item is a linked item.  
  
## Syntax  
  
```  
  
BOOL IsLinkedItem( ) const;  
```  
  
## Return Value  
 Nonzero if the item is a linked item; otherwise 0.  
  
## Remarks  
 An item is linked if the item is valid and is not returned in the document's list of embedded items. A linked item might or might not be connected to a container.  
  
 It is common to use the same class for both linked and embedded items. `IsLinkedItem` allows you to make linked items behave differently than embedded items, although many times the code is common.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleServerItem Class](../vs140/COleServerItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleServerItem::IsConnected](../vs140/COleServerItem--IsConnected.md)   
 [COleLinkingDoc::OnGetLinkedItem](../vs140/COleLinkingDoc--OnGetLinkedItem.md)