---
title: "COleClientItem::IsOpen"
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
ms.assetid: d8f5f2b1-c70b-4921-abe3-fe8c2ca4fd97
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleClientItem::IsOpen
Call this function to see whether the OLE item is open; that is, opened in an instance of the server application running in a separate window.  
  
## Syntax  
  
```  
  
BOOL IsOpen( ) const;  
```  
  
## Return Value  
 Nonzero if the OLE item is open; otherwise 0.  
  
## Remarks  
 It is used to determine when to draw the object with a hatching pattern. An open object should have a hatch pattern drawn on top of the object. You can use a [CRectTracker](../vs140/CRectTracker-Class.md) object to accomplish this.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleClientItem Class](../vs140/COleClientItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleClientItem::GetItemState](../vs140/COleClientItem--GetItemState.md)   
 [CRectTracker Class](../vs140/CRectTracker-Class.md)