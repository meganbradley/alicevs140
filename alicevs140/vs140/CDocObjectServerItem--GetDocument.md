---
title: "CDocObjectServerItem::GetDocument"
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
ms.assetid: 32ea1efc-cc0d-4c85-8af4-fa12149ffbf0
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDocObjectServerItem::GetDocument
Retrieves a pointer to the document that contains the item.  
  
## Syntax  
  
```  
  
COleServerDoc* GetDocument( ) const;  
  
```  
  
## Return Value  
 A pointer to the document that contains the item; **NULL** if the item is not part of a document.  
  
## Remarks  
 This allows access to the server document that you passed as an argument to the [CDocObjectServerItem](../vs140/CDocObjectServerItem--CDocObjectServerItem.md) constructor.  
  
## Requirements  
 **Header:** afxdocob.h  
  
## See Also  
 [CDocObjectServerItem Class](../vs140/CDocObjectServerItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDocObjectServer Class](../vs140/CDocObjectServer-Class.md)