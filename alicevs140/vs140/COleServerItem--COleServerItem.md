---
title: "COleServerItem::COleServerItem"
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
ms.assetid: f7fb2ea5-ab07-466a-95f9-7d848d52da4e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleServerItem::COleServerItem
Constructs a `COleServerItem` object and adds it to the server document's collection of document items.  
  
## Syntax  
  
```  
  
      COleServerItem(  
   COleServerDoc* pServerDoc,  
   BOOL bAutoDelete   
);  
```  
  
#### Parameters  
 `pServerDoc`  
 Pointer to the document that will contain the new item.  
  
 `bAutoDelete`  
 Flag indicating whether the object can be deleted when a link to it is released. Set this to **FALSE** if the `COleServerItem` object is an integral part of your document's data which you must delete. Set this to **TRUE** if the object is a secondary structure used to identify a range in your document's data that can be deleted by the framework.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleServerItem Class](../vs140/COleServerItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDocument::AddItem](../vs140/COleDocument--AddItem.md)