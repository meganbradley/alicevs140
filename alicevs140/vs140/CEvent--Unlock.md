---
title: "CEvent::Unlock"
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
ms.assetid: 88e899c8-fe94-48bb-bd2d-138c629db062
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CEvent::Unlock
Releases the event object.  
  
## Syntax  
  
```  
  
BOOL Unlock( );  
  
```  
  
## Return Value  
 Nonzero if the thread owned the event object and the event is an automatic event; otherwise 0.  
  
## Remarks  
 This member function is called by threads that currently own an automatic event to release it after they are done, if their lock object is to be reused. If the lock object is not to be reused, this function will be called by the lock object's destructor.  
  
## Requirements  
 **Header:** afxmt.h  
  
## See Also  
 [CEvent Class](../vs140/CEvent-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)