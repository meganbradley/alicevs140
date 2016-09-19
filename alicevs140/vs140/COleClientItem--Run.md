---
title: "COleClientItem::Run"
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
ms.assetid: 1ff40232-bb2c-464f-84b5-9896d739e7b2
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleClientItem::Run
Runs the application associated with this item.  
  
## Syntax  
  
```  
  
void Run( );  
```  
  
## Remarks  
 Call the **Run** member function to launch the server application before activating the item. This is done automatically by [Activate](../vs140/COleClientItem--Activate.md) and [DoVerb](../vs140/COleClientItem--DoVerb.md), so it is usually not necessary to call this function. Call this function if it is necessary to run the server in order to set an item attribute, such as [SetExtent](../vs140/COleClientItem--SetExtent.md), before executing [DoVerb](../vs140/COleClientItem--DoVerb.md).  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleClientItem Class](../vs140/COleClientItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleClientItem::IsRunning](../vs140/COleClientItem--IsRunning.md)