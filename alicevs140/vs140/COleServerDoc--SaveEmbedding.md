---
title: "COleServerDoc::SaveEmbedding"
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
ms.assetid: afda10b8-0ff3-4812-a4e3-1863c208ed5c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleServerDoc::SaveEmbedding
Call this function to tell the container application to save the embedded object.  
  
## Syntax  
  
```  
  
void SaveEmbedding( );  
```  
  
## Remarks  
 This function is called automatically from `OnUpdateDocument`. Note that this function causes the item to be updated on disk, so it is usually called only as a result of a specific user action.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleServerDoc Class](../vs140/COleServerDoc-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleServerDoc::NotifyClosed](../vs140/COleServerDoc--NotifyClosed.md)