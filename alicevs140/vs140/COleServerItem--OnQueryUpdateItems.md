---
title: "COleServerItem::OnQueryUpdateItems"
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
ms.assetid: 73793692-dafd-49b8-a04d-d0a01199d7bb
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleServerItem::OnQueryUpdateItems
Called by the framework to determine whether any linked items in the current server document are out of date.  
  
## Syntax  
  
```  
  
virtual BOOL OnQueryUpdateItems( );  
```  
  
## Return Value  
 Nonzero if the document has items needing updates; 0 if all items are up to date.  
  
## Remarks  
 An item is out of date if its source document has been changed but the linked item has not been updated to reflect the changes in the document.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleServerItem Class](../vs140/COleServerItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleServerItem::OnUpdate](../vs140/COleServerItem--OnUpdate.md)   
 [COleServerItem::OnUpdateItems](../vs140/COleServerItem--OnUpdateItems.md)