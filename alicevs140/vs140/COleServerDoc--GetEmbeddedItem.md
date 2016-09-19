---
title: "COleServerDoc::GetEmbeddedItem"
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
ms.assetid: 38a42500-dbbb-42fd-8e2a-6eb5cb453819
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleServerDoc::GetEmbeddedItem
Call this function to get a pointer to an item representing the entire document.  
  
## Syntax  
  
```  
  
COleServerItem* GetEmbeddedItem( );  
```  
  
## Return Value  
 A pointer to an item representing the entire document; **NULL** if the operation failed.  
  
## Remarks  
 It calls [COleServerDoc::OnGetEmbeddedItem](../vs140/COleServerDoc--OnGetEmbeddedItem.md), a virtual function with no default implementation.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleServerDoc Class](../vs140/COleServerDoc-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleServerDoc::OnGetEmbeddedItem](../vs140/COleServerDoc--OnGetEmbeddedItem.md)