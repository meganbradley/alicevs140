---
title: "COleClientItem::CreateCloneFrom"
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
ms.assetid: 9dd94c31-8d6f-414b-88eb-e0d22f842db1
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleClientItem::CreateCloneFrom
Call this function to create a copy of the specified OLE item.  
  
## Syntax  
  
```  
  
      BOOL CreateCloneFrom(  
   const COleClientItem* pSrcItem   
);  
```  
  
#### Parameters  
 *pSrcItem*  
 Pointer to the OLE item to be duplicated.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 The copy is identical to the source item. You can use this function to support undo operations.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleClientItem Class](../vs140/COleClientItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleClientItem::CreateNewItem](../vs140/COleClientItem--CreateNewItem.md)