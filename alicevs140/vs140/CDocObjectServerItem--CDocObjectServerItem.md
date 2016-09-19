---
title: "CDocObjectServerItem::CDocObjectServerItem"
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
ms.assetid: 8585d9a3-90ec-4b41-807a-11673aa36b23
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDocObjectServerItem::CDocObjectServerItem
Constructs a `CDocObjectServerItem` object.  
  
## Syntax  
  
```  
  
      CDocObjectServerItem(  
   COleServerDoc* pServerDoc,  
   BOOL bAutoDelete   
);  
```  
  
#### Parameters  
 `pServerDoc`  
 A pointer to the document that will contain the new DocObject item.  
  
 `bAutoDelete`  
 Indicates whether the object can be deleted when a link to it is released. Set the argument to **FALSE** if the `CDocObjectServerItem` object is an integral part of your document's data. Set it to **TRUE** if the object is a secondary structure used to identify a range in your document's data that can be deleted by the framework.  
  
## Requirements  
 **Header:** afxdocob.h  
  
## See Also  
 [CDocObjectServerItem Class](../vs140/CDocObjectServerItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDocObjectServer Class](../vs140/CDocObjectServer-Class.md)