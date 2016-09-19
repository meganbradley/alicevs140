---
title: "COleDocument::GetStartPosition"
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
ms.assetid: 512d0652-ffe3-46e8-9a9d-37bdc14a797a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDocument::GetStartPosition
Call this function to get the position of the first item in the document.  
  
## Syntax  
  
```  
  
virtual POSITION GetStartPosition( ) const;  
```  
  
## Return Value  
 A **POSITION** value that can be used to begin iterating through the document's items; **NULL** if the document has no items.  
  
## Remarks  
 Pass the value returned to `GetNextItem`, `GetNextClientItem`, or `GetNextServerItem`.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleDocument Class](../vs140/COleDocument-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDocument::GetNextItem](../vs140/COleDocument--GetNextItem.md)   
 [COleDocument::GetNextClientItem](../vs140/COleDocument--GetNextClientItem.md)   
 [COleDocument::GetNextServerItem](../vs140/COleDocument--GetNextServerItem.md)