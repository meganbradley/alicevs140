---
title: "COleServerItem::SetItemName"
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
ms.assetid: 3f952d9b-800a-459d-8b9d-9f7db8ccf01a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleServerItem::SetItemName
Call this function when you create a linked item to set its name.  
  
## Syntax  
  
```  
  
      void SetItemName(  
   LPCTSTR lpszItemName   
);  
```  
  
#### Parameters  
 `lpszItemName`  
 Pointer to the new name of the item.  
  
## Remarks  
 The name must be unique within the document. When a server application is called to edit a linked item, the application uses this name to find the item. You do not need to call this function for embedded items.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleServerItem Class](../vs140/COleServerItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleServerItem::GetItemName](../vs140/COleServerItem--GetItemName.md)   
 [COleLinkingDoc::OnGetLinkedItem](../vs140/COleLinkingDoc--OnGetLinkedItem.md)