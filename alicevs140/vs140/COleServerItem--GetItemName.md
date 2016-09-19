---
title: "COleServerItem::GetItemName"
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
ms.assetid: d60be1f9-6f16-4aa0-8707-1799dd5b5382
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleServerItem::GetItemName
Call this function to get the name of the item.  
  
## Syntax  
  
```  
  
const CString& GetItemName( ) const;  
```  
  
## Return Value  
 The name of the item.  
  
## Remarks  
 You typically call this function only for linked items.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleServerItem Class](../vs140/COleServerItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleServerItem::SetItemName](../vs140/COleServerItem--SetItemName.md)   
 [COleLinkingDoc::OnGetLinkedItem](../vs140/COleLinkingDoc--OnGetLinkedItem.md)