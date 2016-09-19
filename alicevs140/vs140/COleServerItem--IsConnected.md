---
title: "COleServerItem::IsConnected"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: b2888a50-472b-4e31-a074-b1d0ad95bca3
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleServerItem::IsConnected
Call this function to see if the OLE item is connected.  
  
## Syntax  
  
```  
  
BOOL IsConnected( ) const;  
```  
  
## Return Value  
 Nonzero if the item is connected; otherwise 0.  
  
## Remarks  
 An OLE item is considered connected if one or more containers have references to the item. An item is connected if its reference count is greater than 0 or if it is an embedded item.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleServerItem Class](../vs140/COleServerItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleServerItem::IsLinkedItem](../vs140/COleServerItem--IsLinkedItem.md)   
 [COleLinkingDoc::OnGetLinkedItem](../vs140/COleLinkingDoc--OnGetLinkedItem.md)