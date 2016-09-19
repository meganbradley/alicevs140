---
title: "COleDocument::RemoveItem"
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
ms.assetid: ee245182-1bbb-4ed0-bdad-2c647a484a0b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDocument::RemoveItem
Call this function to remove an item from the document.  
  
## Syntax  
  
```  
  
      virtual void RemoveItem(  
   CDocItem* pItem   
);  
```  
  
#### Parameters  
 `pItem`  
 Pointer to the document item to be removed.  
  
## Remarks  
 You typically do not need to call this function explicitly; it is called by the destructors for `COleClientItem` and `COleServerItem`.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleDocument Class](../vs140/COleDocument-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleServerItem Class](../vs140/COleServerItem-Class.md)   
 [COleClientItem Class](../vs140/COleClientItem-Class.md)   
 [COleDocument::AddItem](../vs140/COleDocument--AddItem.md)   
 [CDocItem Class](../vs140/CDocItem-Class.md)