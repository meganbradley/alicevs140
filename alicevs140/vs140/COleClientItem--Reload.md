---
title: "COleClientItem::Reload"
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
ms.assetid: ce6d9b68-2bbc-47ae-9335-33b58db568c8
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleClientItem::Reload
Closes and reloads the item.  
  
## Syntax  
  
```  
  
BOOL Reload( );  
```  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 Call the `Reload` function after activating the item as an item of another type by a call to [ActivateAs](../vs140/COleClientItem--ActivateAs.md).  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleClientItem Class](../vs140/COleClientItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleClientItem::ActivateAs](../vs140/COleClientItem--ActivateAs.md)