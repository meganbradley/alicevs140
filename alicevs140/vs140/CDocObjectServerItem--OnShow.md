---
title: "CDocObjectServerItem::OnShow"
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
ms.assetid: c156e330-aaa8-49ca-b419-1459d219840b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDocObjectServerItem::OnShow
Called by the framework to instruct the server application to make the DocObject item in-place active.  
  
## Syntax  
  
```  
  
virtual void OnShow( );  
```  
  
## Remarks  
 If the item is not a DocObject, the default implementation calls [COleServerItem::OnShow](../vs140/COleServerItem--OnOpen.md). Override this function if you want to perform special processing when opening a DocObject item.  
  
## Requirements  
 **Header:** afxdocob.h  
  
## See Also  
 [CDocObjectServerItem Class](../vs140/CDocObjectServerItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDocObjectServerItem::OnHide](../vs140/CDocObjectServerItem--OnHide.md)   
 [CDocObjectServerItem::OnOpen](assetId:///7a9b1363-6ad8-4732-9959-4e35c07644fd)