---
title: "COleServerDoc::DeactivateAndUndo"
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
ms.assetid: 7cbaa7db-4a55-4f3e-87fd-f3cb7c258840
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleServerDoc::DeactivateAndUndo
Call this function if your application supports Undo and the user chooses Undo after activating an item but before editing it.  
  
## Syntax  
  
```  
  
BOOL DeactivateAndUndo( );  
```  
  
## Return Value  
 Nonzero on success; otherwise 0.  
  
## Remarks  
 If the container application is written using the Microsoft Foundation Class Library, calling this function causes [COleClientItem::OnDeactivateAndUndo](../vs140/COleClientItem--OnDeactivateAndUndo.md) to be called, which deactivates the server's user interface.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleServerDoc Class](../vs140/COleServerDoc-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleClientItem::OnDeactivateAndUndo](../vs140/COleClientItem--OnDeactivateAndUndo.md)