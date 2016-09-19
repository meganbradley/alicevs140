---
title: "COleServerItem::GetDocument"
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
ms.assetid: b7bb0be5-233d-4998-b78f-f5e1a3136dd1
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleServerItem::GetDocument
Call this function to get a pointer to the document that contains the item.  
  
## Syntax  
  
```  
  
COleServerDoc* GetDocument( ) const;  
```  
  
## Return Value  
 A pointer to the document that contains the item; **NULL** if the item is not part of a document.  
  
## Remarks  
 This allows access to the server document that you passed as an argument to the `COleServerItem` constructor.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleServerItem Class](../vs140/COleServerItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleServerItem::COleServerItem](../vs140/COleServerItem--COleServerItem.md)   
 [COleServerDoc Class](../vs140/COleServerDoc-Class.md)