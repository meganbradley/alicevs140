---
title: "COleServerItem::OnUpdateItems"
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
ms.assetid: f7f61a27-f1a3-4527-98f7-f524dcbb0114
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleServerItem::OnUpdateItems
Called by the framework to update all items in the server document.  
  
## Syntax  
  
```  
  
virtual void OnUpdateItems( );  
```  
  
## Remarks  
 The default implementation calls [UpdateLink](../vs140/COleClientItem--UpdateLink.md) for all `COleClientItem` objects in the document.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleServerItem Class](../vs140/COleServerItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleServerItem::OnUpdate](../vs140/COleServerItem--OnUpdate.md)   
 [COleServerItem::OnQueryUpdateItems](../vs140/COleServerItem--OnQueryUpdateItems.md)