---
title: "COleClientItem::GetDocument"
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
ms.assetid: 5fc698b9-727f-4eda-8413-53a90e2f462f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleClientItem::GetDocument
Call this function to get a pointer to the document that contains the OLE item.  
  
## Syntax  
  
```  
  
COleDocument* GetDocument( ) const;  
```  
  
## Return Value  
 A pointer to the document that contains the OLE item. **NULL** if the item is not part of a document.  
  
## Remarks  
 This pointer allows access to the `COleDocument` object that you passed as an argument to the `COleClientItem` constructor.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleClientItem Class](../vs140/COleClientItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleClientItem::COleClientItem](../vs140/COleClientItem--COleClientItem.md)   
 [COleDocument Class](../vs140/COleDocument-Class.md)   
 [COleLinkingDoc Class](../vs140/COleLinkingDoc-Class.md)