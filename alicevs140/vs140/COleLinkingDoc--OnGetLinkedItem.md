---
title: "COleLinkingDoc::OnGetLinkedItem"
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
ms.assetid: 48fd246a-ae87-451a-be9f-16d8cd01731a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleLinkingDoc::OnGetLinkedItem
Called by the framework to check whether the document contains a linked server item with the specified name.  
  
## Syntax  
  
```  
  
      virtual COleServerItem* OnGetLinkedItem(  
   LPCTSTR lpszItemName   
);  
```  
  
#### Parameters  
 `lpszItemName`  
 Pointer to the name of the linked OLE item requested.  
  
## Return Value  
 A pointer to the specified item; **NULL** if the item is not found.  
  
## Remarks  
 The default `COleLinkingDoc` implementation always returns **NULL**. This function is overriden in the derived class `COleServerDoc` to search the list of OLE server items for a linked item with the specified name (the name comparison is case sensitive). Override this function if you have implemented your own method of storing or retrieving linked server items.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleLinkingDoc Class](../vs140/COleLinkingDoc-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleServerItem::GetItemName](../vs140/COleServerItem--GetItemName.md)   
 [COleServerItem::SetItemName](../vs140/COleServerItem--SetItemName.md)   
 [COleLinkingDoc::OnFindEmbeddedItem](../vs140/COleLinkingDoc--OnFindEmbeddedItem.md)