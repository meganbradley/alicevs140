---
title: "COleDocObjectItem::COleDocObjectItem"
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
ms.assetid: 7d65cea6-5c1d-4467-a176-52e135de0820
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDocObjectItem::COleDocObjectItem
Call this member function to initialize the `COleDocObjectItem` object.  
  
## Syntax  
  
```  
  
      COleDocObjectItem(  
   COleDocument* pContainerDoc = NULL   
);  
```  
  
#### Parameters  
 `pContainerDoc`  
 A pointer to the `COleDocument` object acting as the active document container. This parameter must be **NULL** to enable **IMPLEMENT_SERIALIZE**. Normally OLE items are constructed with a non-**NULL** document pointer.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleDocObjectItem Class](../vs140/COleDocObjectItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)